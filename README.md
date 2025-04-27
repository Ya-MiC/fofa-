下面给出一条专门用来搜索「既是家庭宽带 IP（Residential ISP），又通过 Cloudflare 反向代理」的 FOFA 语句示例，你可以按此格式替换国家和运营商名称／ASN 使用：

```plaintext
header="cloudflare" && country="KR" && isp="SK Broadband Co Ltd" && status_code="403"
```

- `header="cloudflare"`：筛选 Cloudflare 反代节点  
- `country="KR"`：限定在韩国  
- `isp="SK Broadband Co Ltd"`：只选家庭宽带运营商 SK Broadband  
- `status_code="403"`：通常 403 返回更稳定、不可直接访问的反代节点  

---

## 如何在 16 个国家做同样的搜索

只要把 `country` 和 `isp` 两个字段改成目标国家／运营商即可。下面按前面列出的 16 国主要 ISP 给出完整示例——每个国家一条语句：

```plaintext
// 1. 新加坡 (SG)
header="cloudflare" && country="SG" && isp="Singtel" && status_code="403"

// 2. 新西兰 (NZ)
header="cloudflare" && country="NZ" && isp="Spark New Zealand" && status_code="403"

// 3. 韩国 (KR)
header="cloudflare" && country="KR" && isp="SK Broadband Co Ltd" && status_code="403"

// 4. 日本 (JP)
header="cloudflare" && country="JP" && isp="NTT Communications" && status_code="403"

// 5. 英国 (GB)
header="cloudflare" && country="GB" && isp="British Telecommunications" && status_code="403"

// 6. 法国 (FR)
header="cloudflare" && country="FR" && isp="Orange S.A." && status_code="403"

// 7. 德国 (DE)
header="cloudflare" && country="DE" && isp="Deutsche Telekom" && status_code="403"

// 8. 美国 (US)
header="cloudflare" && country="US" && isp="Comcast" && status_code="403"

// 9. 加拿大 (CA)
header="cloudflare" && country="CA" && isp="Bell Canada" && status_code="403"

// 10. 香港 (HK)
header="cloudflare" && country="HK" && isp="PCCW Global" && status_code="403"

// 11. 台湾 (TW)
header="cloudflare" && country="TW" && isp="Chunghwa Telecom" && status_code="403"

// 12. 荷兰 (NL)
header="cloudflare" && country="NL" && isp="KPN B.V." && status_code="403"

// 13. 挪威 (NO)
header="cloudflare" && country="NO" && isp="Telenor Norway" && status_code="403"

// 14. 瑞士 (CH)
header="cloudflare" && country="CH" && isp="Swisscom" && status_code="403"

// 15. 波兰 (PL)
header="cloudflare" && country="PL" && isp="Orange Polska" && status_code="403"

// 16. 阿联酋 (AE)
header="cloudflare" && country="AE" && isp="Etisalat (UAE)" && status_code="403"
```

> **说明**  
> - 如果你更习惯用 ASN 过滤，也可以把 `isp="…" ` 换成 `asn="XXXX"`。  
> - 若要切换到返回 406 状态，只需把 `status_code="403"` 改成 `status_code="406"`。  
> - 以上语句均可直接复制到 FOFA 搜索框使用。  

这样，你就能一键在各地 ISP 中挑出那些家宽级别的、同时被 Cloudflare 反代的高质量 IP。
