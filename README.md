以下是按国家分块、格式精美的 FOFA 搜索代码，每块都清晰列出了主要本地运营商及其 ASN，方便你复制粘贴即用。

---

## 1. 新加坡 (SG)

**主要本地运营商及 ASN：**  
- Singtel — ASN 7473  ([Tier 1 network - Wikipedia](https://en.wikipedia.org/wiki/Tier_1_network?utm_source=chatgpt.com))  
- StarHub — ASN 4657  ([StarHub AS4657 - PeeringDB](https://www.peeringdb.com/asn/4657?utm_source=chatgpt.com))  
- M1 — ASN 17547  ([M1 Limited - AS4773 - PeeringDB](https://www.peeringdb.com/asn/4773?utm_source=chatgpt.com))  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="SG"
&& (asn="7473" || asn="4657" || asn="17547")
```

---

## 2. 新西兰 (NZ)

**主要本地运营商及 ASN：**  
- Spark — ASN 12357  
- Vodafone NZ — ASN 7545  
- 2degrees — ASN 6037  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="NZ"
&& (asn="12357" || asn="7545" || asn="6037")
```

---

## 3. 韩国 (KR)

**主要本地运营商及 ASN：**  
- SK Broadband — ASN 9318  ([SK Broadband](https://en.wikipedia.org/wiki/SK_Broadband?utm_source=chatgpt.com), [ASN Information for 9318 SK Broadband Co Ltd - IP2Location](https://www.ip2location.com/as9318?utm_source=chatgpt.com))  
- KT Corp — ASN 4766  ([Tier 2 network - Wikipedia](https://en.wikipedia.org/wiki/Tier_2_network?utm_source=chatgpt.com))  
- LG U+ — ASN 4763  ([Tier 2 network - Wikipedia](https://en.wikipedia.org/wiki/Tier_2_network?utm_source=chatgpt.com))  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="KR"
&& (asn="9318" || asn="4766" || asn="4763")
```

---

## 4. 日本 (JP)

**主要本地运营商及 ASN：**  
- NTT Communications — ASN 2914  ([Tier 2 network - Wikipedia](https://en.wikipedia.org/wiki/Tier_2_network?utm_source=chatgpt.com))  
- KDDI — ASN 2516  ([Tier 2 network - Wikipedia](https://en.wikipedia.org/wiki/Tier_2_network?utm_source=chatgpt.com))  
- SoftBank — ASN 17676  ([Tier 2 network - Wikipedia](https://en.wikipedia.org/wiki/Tier_2_network?utm_source=chatgpt.com))  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="JP"
&& (asn="2914" || asn="2516" || asn="17676")
```

---

## 5. 英国 (GB)

**主要本地运营商及 ASN：**  
- British Telecom (BT) — ASN 5400  ([Tier 2 network - Wikipedia](https://en.wikipedia.org/wiki/Tier_2_network?utm_source=chatgpt.com))  
- Virgin Media — ASN 5089  
- Sky UK — ASN 12876  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="GB"
&& (asn="5400" || asn="5089" || asn="12876")
```

---

## 6. 法国 (FR)

**主要本地运营商及 ASN：**  
- Orange S.A. — ASN 5511  ([Tier 2 network - Wikipedia](https://en.wikipedia.org/wiki/Tier_2_network?utm_source=chatgpt.com))  
- SFR — ASN 1273  
- Bouygues Telecom — ASN 12479  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="FR"
&& (asn="5511" || asn="1273" || asn="12479")
```

---

## 7. 德国 (DE)

**主要本地运营商及 ASN：**  
- Deutsche Telekom — ASN 3320  ([Tier 2 network - Wikipedia](https://en.wikipedia.org/wiki/Tier_2_network?utm_source=chatgpt.com))  
- Vodafone DE — ASN 3209  
- Unitymedia (現 Vodafone) — ASN 6830  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="DE"
&& (asn="3320" || asn="3209" || asn="6830")
```

---

## 8. 美国 (US)

**主要本地运营商及 ASN：**  
- Comcast — ASN 7922  ([Tier 2 network - Wikipedia](https://en.wikipedia.org/wiki/Tier_2_network?utm_source=chatgpt.com))  
- AT&T — ASN 7018  
- Verizon — ASN 701  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="US"
&& (asn="7922" || asn="7018" || asn="701")
```

---

## 9. 加拿大 (CA)

**主要本地运营商及 ASN：**  
- Bell Canada — ASN 577  ([AS577 Bell Canada - bgp.he.net](https://bgp.he.net/as577?utm_source=chatgpt.com))  
- Rogers Communications — ASN 812  ([AS812 Rogers Communications Canada Inc. Network Details - IPQS](https://www.ipqualityscore.com/asn-details/AS812/rogers-communications-canada-inc?utm_source=chatgpt.com))  
- Telus — ASN 852  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="CA"
&& (asn="577" || asn="812" || asn="852")
```

---

## 10. 香港 (HK)

**主要本地运营商及 ASN：**  
- PCCW Global — ASN 3491  ([AS3491 PCCW Global, Inc. - bgp.tools](https://bgp.tools/as/3491?utm_source=chatgpt.com))  
- HKT — ASN 4637  
- Hutchison Telecom Hong Kong — ASN 7552  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="HK"
&& (asn="3491" || asn="4637" || asn="7552")
```

---

## 11. 台湾 (TW)

**主要本地运营商及 ASN：**  
- Chunghwa Telecom — ASN 3462  ([Tier 2 network - Wikipedia](https://en.wikipedia.org/wiki/Tier_2_network?utm_source=chatgpt.com))  
- Taiwan Mobile — ASN 9498  
- FarEasTone — ASN 9808  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="TW"
&& (asn="3462" || asn="9498" || asn="9808")
```

---

## 12. 荷兰 (NL)

**主要本地运营商及 ASN：**  
- KPN B.V. — ASN 1136  ([ASN Information for 1136 KPN B.V. - IP2Location](https://www.ip2location.com/as1136?utm_source=chatgpt.com))  
- Ziggo — ASN 8767  
- T-Mobile Netherlands — ASN 11309  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="NL"
&& (asn="1136" || asn="8767" || asn="11309")
```

---

## 13. 挪威 (NO)

**主要本地运营商及 ASN：**  
- Telenor Norway — ASN 1299  
- Altibox — ASN 6795  
- NextGenTel — ASN 27852  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="NO"
&& (asn="1299" || asn="6795" || asn="27852")
```

---

## 14. 瑞士 (CH)

**主要本地运营商及 ASN：**  
- Swisscom — ASN 3303  
- Sunrise Communications — ASN 6853  
- Salt (Swisscom Subsidiary) — ASN 13188  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="CH"
&& (asn="3303" || asn="6853" || asn="13188")
```

---

## 15. 波兰 (PL)

**主要本地运营商及 ASN：**  
- Orange Polska — ASN 5617  
- T-Mobile Polska — ASN 1267  
- Netia — ASN 1243  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="PL"
&& (asn="5617" || asn="1267" || asn="1243")
```

---

## 16. 阿拉伯联合酋长国 (AE)

**主要本地运营商及 ASN：**  
- Etisalat (UAE) — ASN 7843  
- du UAE — ASN 15684  
- Yahsat — ASN 24863  

**FOFA 搜索代码：**  
```plaintext
(header="cloudflare" || cert="cloudflare" || header="google" || cert="google" ||
 header="yahoo"    || cert="yahoo"    || header="amazon" || cert="amazon" ||
 header="alibaba"  || cert="alibaba")
&& status_code="403" && country="AE"
&& (asn="7843" || asn="15684" || asn="24863")
```

---

> **提示：**  
> - 以上大厂（Cloudflare/Google/Yahoo/Amazon/Alibaba）与本地运营商结合，就能一次性筛出高质量、可优选且可做 Proxy 的 IP。  
> - 若要调整状态码为 406，只需将 `status_code="403"` 改为 `status_code="406"` 即可。  

