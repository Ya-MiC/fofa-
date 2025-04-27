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

以下内容将帮助你在 16 个国家/地区中，精准搜索「既是家庭宽带 ISP 级别 IP，又通过 Amazon CloudFront 反向代理」的高质量节点。总结段落中会概括关键要点，之后按国家分别给出可直接复制粘贴的 FOFA 语句。

## 概要

你要的节点需同时满足以下条件：  
1. **家庭宽带 ISP 级别**：使用 `isp="…" ` 或 `asn="…" ` 精确定位当地主流家庭宽带运营商。  
2. **Amazon CloudFront 反向代理**：匹配 `header="cloudfront"`，因为 CloudFront 默认会在响应中添加 `Server: CloudFront` 头部 ([Understand response headers policies - Amazon CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/understanding-response-headers-policies.html?utm_source=chatgpt.com))。  
3. **排除官方 AWS 网络**：通过 `asn!="16509"` 排除 AWS 自身 AS16509，以确保找到的是第三方或 ISP 层面的边缘节点。  
4. **安全状态码**：常用 `status_code="403"` 或可替换为 `406`，以筛选受保护的反代接口。

下面给出每个国家的示例语句——可直接复制到 FOFA 搜索框使用。

---

## 1. 新加坡 (SG)

```plaintext
header="cloudfront" && status_code="403" && country="SG" && isp="Singtel" && asn!="16509"
header="cloudfront" && status_code="403" && country="SG" && isp="StarHub"  && asn!="16509"
header="cloudfront" && status_code="403" && country="SG" && isp="M1"       && asn!="16509"
```

---

## 2. 新西兰 (NZ)

```plaintext
header="cloudfront" && status_code="403" && country="NZ" && isp="Spark New Zealand" && asn!="16509"
header="cloudfront" && status_code="403" && country="NZ" && isp="Vodafone NZ"      && asn!="16509"
header="cloudfront" && status_code="403" && country="NZ" && isp="2degrees"         && asn!="16509"
```

---

## 3. 韩国 (KR)

```plaintext
header="cloudfront" && status_code="403" && country="KR" && isp="SK Broadband Co Ltd" && asn!="16509"
header="cloudfront" && status_code="403" && country="KR" && isp="KT Corp"             && asn!="16509"
header="cloudfront" && status_code="403" && country="KR" && isp="LG U+"              && asn!="16509"
```

---

## 4. 日本 (JP)

```plaintext
header="cloudfront" && status_code="403" && country="JP" && isp="NTT Communications" && asn!="16509"
header="cloudfront" && status_code="403" && country="JP" && isp="KDDI"               && asn!="16509"
header="cloudfront" && status_code="403" && country="JP" && isp="SoftBank"           && asn!="16509"
```

---

## 5. 英国 (GB)

```plaintext
header="cloudfront" && status_code="403" && country="GB" && isp="British Telecommunications" && asn!="16509"
header="cloudfront" && status_code="403" && country="GB" && isp="Virgin Media"             && asn!="16509"
header="cloudfront" && status_code="403" && country="GB" && isp="Sky UK"                    && asn!="16509"
```

---

## 6. 法国 (FR)

```plaintext
header="cloudfront" && status_code="403" && country="FR" && isp="Orange S.A."            && asn!="16509"
header="cloudfront" && status_code="403" && country="FR" && isp="SFR"                   && asn!="16509"
header="cloudfront" && status_code="403" && country="FR" && isp="Bouygues Telecom"      && asn!="16509"
```

---

## 7. 德国 (DE)

```plaintext
header="cloudfront" && status_code="403" && country="DE" && isp="Deutsche Telekom" && asn!="16509"
header="cloudfront" && status_code="403" && country="DE" && isp="Vodafone DE"      && asn!="16509"
header="cloudfront" && status_code="403" && country="DE" && isp="Unitymedia"       && asn!="16509"
```

---

## 8. 美国 (US)

```plaintext
header="cloudfront" && status_code="403" && country="US" && isp="Comcast"       && asn!="16509"
header="cloudfront" && status_code="403" && country="US" && isp="AT&T"          && asn!="16509"
header="cloudfront" && status_code="403" && country="US" && isp="Verizon"       && asn!="16509"
```

---

## 9. 加拿大 (CA)

```plaintext
header="cloudfront" && status_code="403" && country="CA" && isp="Bell Canada" && asn!="16509"
header="cloudfront" && status_code="403" && country="CA" && isp="Rogers"      && asn!="16509"
header="cloudfront" && status_code="403" && country="CA" && isp="Telus"       && asn!="16509"
```

---

## 10. 香港 (HK)

```plaintext
header="cloudfront" && status_code="403" && country="HK" && isp="PCCW Global"                && asn!="16509"
header="cloudfront" && status_code="403" && country="HK" && isp="HKT"                       && asn!="16509"
header="cloudfront" && status_code="403" && country="HK" && isp="Hutchison Telecom Hong Kong" && asn!="16509"
```

---

## 11. 台湾 (TW)

```plaintext
header="cloudfront" && status_code="403" && country="TW" && isp="Chunghwa Telecom" && asn!="16509"
header="cloudfront" && status_code="403" && country="TW" && isp="Taiwan Mobile"    && asn!="16509"
header="cloudfront" && status_code="403" && country="TW" && isp="FarEasTone"       && asn!="16509"
```

---

## 12. 荷兰 (NL)

```plaintext
header="cloudfront" && status_code="403" && country="NL" && isp="KPN B.V."              && asn!="16509"
header="cloudfront" && status_code="403" && country="NL" && isp="Ziggo"                 && asn!="16509"
header="cloudfront" && status_code="403" && country="NL" && isp="T-Mobile Netherlands" && asn!="16509"
```

---

## 13. 挪威 (NO)

```plaintext
header="cloudfront" && status_code="403" && country="NO" && isp="Telenor Norway" && asn!="16509"
header="cloudfront" && status_code="403" && country="NO" && isp="Altibox"         && asn!="16509"
header="cloudfront" && status_code="403" && country="NO" && isp="NextGenTel"      && asn!="16509"
```

---

## 14. 瑞士 (CH)

```plaintext
header="cloudfront" && status_code="403" && country="CH" && isp="Swisscom"               && asn!="16509"
header="cloudfront" && status_code="403" && country="CH" && isp="Sunrise Communications" && asn!="16509"
header="cloudfront" && status_code="403" && country="CH" && isp="Salt"                  && asn!="16509"
```

---

## 15. 波兰 (PL)

```plaintext
header="cloudfront" && status_code="403" && country="PL" && isp="Orange Polska" && asn!="16509"
header="cloudfront" && status_code="403" && country="PL" && isp="T-Mobile Polska" && asn!="16509"
header="cloudfront" && status_code="403" && country="PL" && isp="Netia"           && asn!="16509"
```

---

## 16. 阿联酋 (AE)

```plaintext
header="cloudfront" && status_code="403" && country="AE" && isp="Etisalat (UAE)" && asn!="16509"
header="cloudfront" && status_code="403" && country="AE" && isp="du UAE"          && asn!="16509"
header="cloudfront" && status_code="403" && country="AE" && isp="Yahsat"          && asn!="16509"
```

---

> **使用提示**：  
> - 若要筛选 `status_code="406"`，可全局替换。  
> - 如需更严格的 ASN 过滤，只保留 `asn="XXXX"` 即可。  
> - 代码块可直接复制到 FOFA 搜索，迅速定位家宽级 Amazon 反代节点。  

Happy hunting!
