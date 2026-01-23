# zap_report_round3

ZAP by [Checkmarx](https://checkmarx.com/).


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 8 |
| Informational | 5 |




## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- |
| Content Security Policy (CSP) Header Not Set | Medium | 5 |
| Cross-Domain Misconfiguration | Medium | 91 |
| Missing Anti-clickjacking Header | Medium | 5 |
| Cookie No HttpOnly Flag | Low | 3 |
| Cookie Without Secure Flag | Low | 3 |
| Cookie without SameSite Attribute | Low | 3 |
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 92 |
| Strict-Transport-Security Header Not Set | Low | 3 |
| Timestamp Disclosure - Unix | Low | 3 |
| X-Content-Type-Options Header Missing | Low | 94 |
| ZAP is Out of Date | Low | 3 |
| Information Disclosure - Suspicious Comments | Informational | 1 |
| Modern Web Application | Informational | 5 |
| Re-examine Cache-control Directives | Informational | 97 |
| Retrieved from Cache | Informational | 4 |
| Session Management Response Identified | Informational | 82 |




## Alert Detail



### [ Content Security Policy (CSP) Header Not Set ](https://www.zaproxy.org/docs/alerts/10038/)



##### Medium (High)

### Description

Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.

* URL: https://stats.csdiilit.com/

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/info

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/robots.txt

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/search

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/sitemap.xml

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``


Instances: 5

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to set the Content-Security-Policy header.

### Reference


* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CSP ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CSP)
* [ https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html)
* [ https://www.w3.org/TR/CSP/ ](https://www.w3.org/TR/CSP/)
* [ https://w3c.github.io/webappsec-csp/ ](https://w3c.github.io/webappsec-csp/)
* [ https://web.dev/articles/csp ](https://web.dev/articles/csp)
* [ https://caniuse.com/#feat=contentsecuritypolicy ](https://caniuse.com/#feat=contentsecuritypolicy)
* [ https://content-security-policy.com/ ](https://content-security-policy.com/)


#### CWE Id: [ 693 ](https://cwe.mitre.org/data/definitions/693.html)


#### WASC Id: 15

#### Source ID: 3

### [ Cross-Domain Misconfiguration ](https://www.zaproxy.org/docs/alerts/10098/)



##### Medium (Medium)

### Description

Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server.

* URL: https://firefox.settings.services.mozilla.com/v1/buckets/main/collections/mfcdm-origins-list/changeset%3F_expected=1750871406038

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `access-control-allow-origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Felo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Felo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2501&elo_max=3000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2501&elo_max=3000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=2501&elo_max=3000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpo&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAGZydEzA&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAGZydEzAgEsQCjFx&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAYmOVUhA&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpojpTaPGXa&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRBy&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRByrrsVCFMt&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRByrrsVCFMtqILYndEb&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRByyHlpRBJs&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIk&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkDyomvtdK&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkhmHhseKB&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkVvjPSGHe&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkyYfgblDo&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXu&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXuFwdlCpWZ&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXuFwdlCpWZksHenaTyekjbtlIDriqHeqSlPHZVtRWzZMgDGCXyMgQMjzSyHseFSOilFKDvcQNKOIiHKMMdvqUgTyTBALnEEAgmpzBimfUPxwpzDXjl&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=ZmJRRbjk&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=ZmJRRbjkMpTqSjIk&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/assets/CSDIILIT_400x400.png

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/assets/faceit_login_button.png

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/assets/index-BaWXMpsB.js

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/assets/index-Dvh_uJtZ.css

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/assets/mainokset/farmskins.png

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/assets/mainokset/skinsauna.png

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/assets/stats_background.png

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/favicon.png

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/info

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/robots.txt

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/search

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`
* URL: https://stats.csdiilit.com/sitemap.xml

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `Access-Control-Allow-Origin: *`
  * Other Info: `The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.`


Instances: 91

### Solution

Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).
Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.

### Reference


* [ https://vulncat.fortify.com/en/detail?category=HTML5&subcategory=Overly%20Permissive%20CORS%20Policy ](https://vulncat.fortify.com/en/detail?category=HTML5&subcategory=Overly%20Permissive%20CORS%20Policy)


#### CWE Id: [ 264 ](https://cwe.mitre.org/data/definitions/264.html)


#### WASC Id: 14

#### Source ID: 3

### [ Missing Anti-clickjacking Header ](https://www.zaproxy.org/docs/alerts/10020/)



##### Medium (Medium)

### Description

The response does not protect against 'ClickJacking' attacks. It should include either Content-Security-Policy with 'frame-ancestors' directive or X-Frame-Options.

* URL: https://stats.csdiilit.com/

  * Method: `GET`
  * Parameter: `x-frame-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/info

  * Method: `GET`
  * Parameter: `x-frame-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/robots.txt

  * Method: `GET`
  * Parameter: `x-frame-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/search

  * Method: `GET`
  * Parameter: `x-frame-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/sitemap.xml

  * Method: `GET`
  * Parameter: `x-frame-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``


Instances: 5

### Solution

Modern Web browsers support the Content-Security-Policy and X-Frame-Options HTTP headers. Ensure one of them is set on all web pages returned by your site/app.
If you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive.

### Reference


* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/X-Frame-Options ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/X-Frame-Options)


#### CWE Id: [ 1021 ](https://cwe.mitre.org/data/definitions/1021.html)


#### WASC Id: 15

#### Source ID: 3

### [ Cookie No HttpOnly Flag ](https://www.zaproxy.org/docs/alerts/10010/)



##### Low (Medium)

### Description

A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.

* URL: https://stats.csdiilit.com/

  * Method: `GET`
  * Parameter: `GAESA`
  * Attack: ``
  * Evidence: `Set-Cookie: GAESA`
  * Other Info: ``
* URL: https://stats.csdiilit.com/robots.txt

  * Method: `GET`
  * Parameter: `GAESA`
  * Attack: ``
  * Evidence: `Set-Cookie: GAESA`
  * Other Info: ``
* URL: https://stats.csdiilit.com/sitemap.xml

  * Method: `GET`
  * Parameter: `GAESA`
  * Attack: ``
  * Evidence: `Set-Cookie: GAESA`
  * Other Info: ``


Instances: 3

### Solution

Ensure that the HttpOnly flag is set for all cookies.

### Reference


* [ https://owasp.org/www-community/HttpOnly ](https://owasp.org/www-community/HttpOnly)


#### CWE Id: [ 1004 ](https://cwe.mitre.org/data/definitions/1004.html)


#### WASC Id: 13

#### Source ID: 3

### [ Cookie Without Secure Flag ](https://www.zaproxy.org/docs/alerts/10011/)



##### Low (Medium)

### Description

A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.

* URL: https://stats.csdiilit.com/

  * Method: `GET`
  * Parameter: `GAESA`
  * Attack: ``
  * Evidence: `Set-Cookie: GAESA`
  * Other Info: ``
* URL: https://stats.csdiilit.com/robots.txt

  * Method: `GET`
  * Parameter: `GAESA`
  * Attack: ``
  * Evidence: `Set-Cookie: GAESA`
  * Other Info: ``
* URL: https://stats.csdiilit.com/sitemap.xml

  * Method: `GET`
  * Parameter: `GAESA`
  * Attack: ``
  * Evidence: `Set-Cookie: GAESA`
  * Other Info: ``


Instances: 3

### Solution

Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.

### Reference


* [ https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html ](https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html)


#### CWE Id: [ 614 ](https://cwe.mitre.org/data/definitions/614.html)


#### WASC Id: 13

#### Source ID: 3

### [ Cookie without SameSite Attribute ](https://www.zaproxy.org/docs/alerts/10054/)



##### Low (Medium)

### Description

A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.

* URL: https://stats.csdiilit.com/

  * Method: `GET`
  * Parameter: `GAESA`
  * Attack: ``
  * Evidence: `Set-Cookie: GAESA`
  * Other Info: ``
* URL: https://stats.csdiilit.com/robots.txt

  * Method: `GET`
  * Parameter: `GAESA`
  * Attack: ``
  * Evidence: `Set-Cookie: GAESA`
  * Other Info: ``
* URL: https://stats.csdiilit.com/sitemap.xml

  * Method: `GET`
  * Parameter: `GAESA`
  * Attack: ``
  * Evidence: `Set-Cookie: GAESA`
  * Other Info: ``


Instances: 3

### Solution

Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.

### Reference


* [ https://datatracker.ietf.org/doc/html/draft-ietf-httpbis-cookie-same-site ](https://datatracker.ietf.org/doc/html/draft-ietf-httpbis-cookie-same-site)


#### CWE Id: [ 1275 ](https://cwe.mitre.org/data/definitions/1275.html)


#### WASC Id: 13

#### Source ID: 3

### [ Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) ](https://www.zaproxy.org/docs/alerts/10037/)



##### Low (Medium)

### Description

The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.

* URL: https://stats.csdiilit.com/

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Felo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Felo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2501&elo_max=3000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2501&elo_max=3000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=2501&elo_max=3000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpo&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAGZydEzA&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAGZydEzAgEsQCjFx&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAYmOVUhA&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpojpTaPGXa&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRBy&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRByrrsVCFMt&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRByrrsVCFMtqILYndEb&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRByyHlpRBJs&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIk&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkDyomvtdK&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkhmHhseKB&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkVvjPSGHe&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkyYfgblDo&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXu&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXuFwdlCpWZ&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXuFwdlCpWZksHenaTyekjbtlIDriqHeqSlPHZVtRWzZMgDGCXyMgQMjzSyHseFSOilFKDvcQNKOIiHKMMdvqUgTyTBALnEEAgmpzBimfUPxwpzDXjl&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=ZmJRRbjk&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=ZmJRRbjkMpTqSjIk&limit=20

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/assets/CSDIILIT_400x400.png

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/assets/faceit_login_button.png

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/assets/index-BaWXMpsB.js

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/assets/index-Dvh_uJtZ.css

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/assets/mainokset/farmskins.png

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/assets/mainokset/skinsauna.png

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/assets/stats_background.png

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/auth/faceit/login

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/auth/me

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/favicon.png

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/info

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/robots.txt

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/search

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``
* URL: https://stats.csdiilit.com/sitemap.xml

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `X-Powered-By: Express`
  * Other Info: ``


Instances: 92

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.

### Reference


* [ https://owasp.org/www-project-web-security-testing-guide/v42/4-Web_Application_Security_Testing/01-Information_Gathering/08-Fingerprint_Web_Application_Framework ](https://owasp.org/www-project-web-security-testing-guide/v42/4-Web_Application_Security_Testing/01-Information_Gathering/08-Fingerprint_Web_Application_Framework)
* [ https://www.troyhunt.com/shhh-dont-let-your-response-headers/ ](https://www.troyhunt.com/shhh-dont-let-your-response-headers/)


#### CWE Id: [ 497 ](https://cwe.mitre.org/data/definitions/497.html)


#### WASC Id: 13

#### Source ID: 3

### [ Strict-Transport-Security Header Not Set ](https://www.zaproxy.org/docs/alerts/10035/)



##### Low (High)

### Description

HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.

* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/12943580-a81c-4c79-bdeb-686df660f244

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/ad5b0ea1-f347-497a-8ee6-bef5e0ff38b7

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/d46569d2-66ff-46c1-9d5d-4ad80a30b482

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: ``


Instances: 3

### Solution

Ensure that your web server, application server, load balancer, etc. is configured to enforce Strict-Transport-Security.

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html ](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html)
* [ https://owasp.org/www-community/Security_Headers ](https://owasp.org/www-community/Security_Headers)
* [ https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security ](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
* [ https://caniuse.com/stricttransportsecurity ](https://caniuse.com/stricttransportsecurity)
* [ https://datatracker.ietf.org/doc/html/rfc6797 ](https://datatracker.ietf.org/doc/html/rfc6797)


#### CWE Id: [ 319 ](https://cwe.mitre.org/data/definitions/319.html)


#### WASC Id: 15

#### Source ID: 3

### [ Timestamp Disclosure - Unix ](https://www.zaproxy.org/docs/alerts/10096/)



##### Low (Low)

### Description

A timestamp was disclosed by the application/web server. - Unix

* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/12943580-a81c-4c79-bdeb-686df660f244

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1765588203`
  * Other Info: `1765588203, which evaluates to: 2025-12-13 03:10:03.`
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/ad5b0ea1-f347-497a-8ee6-bef5e0ff38b7

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1765588203`
  * Other Info: `1765588203, which evaluates to: 2025-12-13 03:10:03.`
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/d46569d2-66ff-46c1-9d5d-4ad80a30b482

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `1765588203`
  * Other Info: `1765588203, which evaluates to: 2025-12-13 03:10:03.`


Instances: 3

### Solution

Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.

### Reference


* [ https://cwe.mitre.org/data/definitions/200.html ](https://cwe.mitre.org/data/definitions/200.html)


#### CWE Id: [ 497 ](https://cwe.mitre.org/data/definitions/497.html)


#### WASC Id: 13

#### Source ID: 3

### [ X-Content-Type-Options Header Missing ](https://www.zaproxy.org/docs/alerts/10021/)



##### Low (Medium)

### Description

The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.

* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/12943580-a81c-4c79-bdeb-686df660f244

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/ad5b0ea1-f347-497a-8ee6-bef5e0ff38b7

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/d46569d2-66ff-46c1-9d5d-4ad80a30b482

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Felo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Felo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2501&elo_max=3000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2501&elo_max=3000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=2501&elo_max=3000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpo&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAGZydEzA&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAGZydEzAgEsQCjFx&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAYmOVUhA&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpojpTaPGXa&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRBy&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRByrrsVCFMt&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRByrrsVCFMtqILYndEb&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRByyHlpRBJs&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIk&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkDyomvtdK&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkhmHhseKB&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkVvjPSGHe&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkyYfgblDo&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXu&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXuFwdlCpWZ&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXuFwdlCpWZksHenaTyekjbtlIDriqHeqSlPHZVtRWzZMgDGCXyMgQMjzSyHseFSOilFKDvcQNKOIiHKMMdvqUgTyTBALnEEAgmpzBimfUPxwpzDXjl&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=ZmJRRbjk&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=ZmJRRbjkMpTqSjIk&limit=20

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/assets/CSDIILIT_400x400.png

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/assets/faceit_login_button.png

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/assets/index-BaWXMpsB.js

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/assets/index-Dvh_uJtZ.css

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/assets/mainokset/farmskins.png

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/assets/mainokset/skinsauna.png

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/assets/stats_background.png

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/auth/me

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/favicon.png

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/info

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/robots.txt

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/search

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`
* URL: https://stats.csdiilit.com/sitemap.xml

  * Method: `GET`
  * Parameter: `x-content-type-options`
  * Attack: ``
  * Evidence: ``
  * Other Info: `This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.
At "High" threshold this scan rule will not alert on client or server error responses.`


Instances: 94

### Solution

Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.
If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.

### Reference


* [ https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/compatibility/gg622941(v=vs.85) ](https://learn.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/compatibility/gg622941(v=vs.85))
* [ https://owasp.org/www-community/Security_Headers ](https://owasp.org/www-community/Security_Headers)


#### CWE Id: [ 693 ](https://cwe.mitre.org/data/definitions/693.html)


#### WASC Id: 15

#### Source ID: 3

### [ ZAP is Out of Date ](https://www.zaproxy.org/docs/alerts/10116/)



##### Low (High)

### Description

The version of ZAP you are using to test your app is out of date and is no longer being updated.
The risk level is set based on how out of date your ZAP version is.

* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/ad5b0ea1-f347-497a-8ee6-bef5e0ff38b7

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `The latest version of ZAP is 2.17.0`
* URL: https://firefox.settings.services.mozilla.com/v1/buckets/main/collections/mfcdm-origins-list/changeset%3F_expected=1750871406038

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `The latest version of ZAP is 2.17.0`
* URL: https://stats.csdiilit.com/favicon.png

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: ``
  * Other Info: `The latest version of ZAP is 2.17.0`


Instances: 3

### Solution

Download the latest version of ZAP from https://www.zaproxy.org/download/ and install it.

### Reference


* [ https://www.zaproxy.org/download/ ](https://www.zaproxy.org/download/)


#### CWE Id: [ 1104 ](https://cwe.mitre.org/data/definitions/1104.html)


#### WASC Id: 45

#### Source ID: 3

### [ Information Disclosure - Suspicious Comments ](https://www.zaproxy.org/docs/alerts/10027/)



##### Informational (Low)

### Description

The response appears to contain suspicious comments which may help an attacker.

* URL: https://stats.csdiilit.com/assets/index-BaWXMpsB.js

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `select`
  * Other Info: `The following pattern was used: \bSELECT\b and was detected in likely comment: "//www.w3.org/2000/svg";case"math":return"http://www.w3.org/1998/Math/MathML";default:return"http://www.w3.org/1999/xhtml"}}funct", see evidence field for the suspicious comment/snippet.`


Instances: 1

### Solution

Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.

### Reference



#### CWE Id: [ 615 ](https://cwe.mitre.org/data/definitions/615.html)


#### WASC Id: 13

#### Source ID: 3

### [ Modern Web Application ](https://www.zaproxy.org/docs/alerts/10109/)



##### Informational (Medium)

### Description

The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.

* URL: https://stats.csdiilit.com/

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script type="module" crossorigin src="/assets/index-BaWXMpsB.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: https://stats.csdiilit.com/info

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script type="module" crossorigin src="/assets/index-BaWXMpsB.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: https://stats.csdiilit.com/robots.txt

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script type="module" crossorigin src="/assets/index-BaWXMpsB.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: https://stats.csdiilit.com/search

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script type="module" crossorigin src="/assets/index-BaWXMpsB.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`
* URL: https://stats.csdiilit.com/sitemap.xml

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<script type="module" crossorigin src="/assets/index-BaWXMpsB.js"></script>`
  * Other Info: `No links have been found while there are scripts, which is an indication that this is a modern web application.`


Instances: 5

### Solution

This is an informational alert and so no changes are required.

### Reference




#### Source ID: 3

### [ Re-examine Cache-control Directives ](https://www.zaproxy.org/docs/alerts/10015/)



##### Informational (Low)

### Description

The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content. For static assets like css, js, or image files this might be intended, however, the resources should be reviewed to ensure that no sensitive content will be cached.

* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/12943580-a81c-4c79-bdeb-686df660f244

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `public, max-age=3600`
  * Other Info: ``
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/ad5b0ea1-f347-497a-8ee6-bef5e0ff38b7

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `public, max-age=3600`
  * Other Info: ``
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/d46569d2-66ff-46c1-9d5d-4ad80a30b482

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `public, max-age=3600`
  * Other Info: ``
* URL: https://firefox.settings.services.mozilla.com/v1/buckets/main/collections/mfcdm-origins-list/changeset%3F_expected=1750871406038

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `max-age=3600`
  * Other Info: ``
* URL: https://stats.csdiilit.com/

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private, max-age=0`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Felo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Felo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2501&elo_max=3000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2501&elo_max=3000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=2501&elo_max=3000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpo&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpo&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAGZydEzA&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAGZydEzA&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAGZydEzAgEsQCjFx&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAGZydEzAgEsQCjFx&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAYmOVUhA&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpojpTaPGXa&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRBy&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRByrrsVCFMt&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRByrrsVCFMtqILYndEb&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRByyHlpRBJs&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIk&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIk&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkDyomvtdK&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkDyomvtdK&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkhmHhseKB&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkhmHhseKB&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkVvjPSGHe&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkyYfgblDo&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXu&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXuFwdlCpWZ&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXuFwdlCpWZksHenaTyekjbtlIDriqHeqSlPHZVtRWzZMgDGCXyMgQMjzSyHseFSOilFKDvcQNKOIiHKMMdvqUgTyTBALnEEAgmpzBimfUPxwpzDXjl&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=ZmJRRbjk&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/api/players/search%3Fq=ZmJRRbjkMpTqSjIk&limit=20

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/auth/me

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: ``
  * Other Info: ``
* URL: https://stats.csdiilit.com/auth/me

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private`
  * Other Info: ``
* URL: https://stats.csdiilit.com/info

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private, max-age=0`
  * Other Info: ``
* URL: https://stats.csdiilit.com/robots.txt

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private, max-age=0`
  * Other Info: ``
* URL: https://stats.csdiilit.com/search

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private, max-age=0`
  * Other Info: ``
* URL: https://stats.csdiilit.com/sitemap.xml

  * Method: `GET`
  * Parameter: `cache-control`
  * Attack: ``
  * Evidence: `private, max-age=0`
  * Other Info: ``


Instances: 97

### Solution

For secure content, ensure the cache-control HTTP header is set with "no-cache, no-store, must-revalidate". If an asset should be cached consider setting the directives "public, max-age, immutable".

### Reference


* [ https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching ](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching)
* [ https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Cache-Control ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Cache-Control)
* [ https://grayduck.mn/2021/09/13/cache-control-recommendations/ ](https://grayduck.mn/2021/09/13/cache-control-recommendations/)


#### CWE Id: [ 525 ](https://cwe.mitre.org/data/definitions/525.html)


#### WASC Id: 13

#### Source ID: 3

### [ Retrieved from Cache ](https://www.zaproxy.org/docs/alerts/10050/)



##### Informational (Medium)

### Description

The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.

* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/12943580-a81c-4c79-bdeb-686df660f244

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HIT`
  * Other Info: ``
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/ad5b0ea1-f347-497a-8ee6-bef5e0ff38b7

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HIT`
  * Other Info: ``
* URL: https://firefox-settings-attachments.cdn.mozilla.net/main-workspace/tracking-protection-lists/d46569d2-66ff-46c1-9d5d-4ad80a30b482

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HIT`
  * Other Info: ``
* URL: https://firefox.settings.services.mozilla.com/v1/buckets/main/collections/mfcdm-origins-list/changeset%3F_expected=1750871406038

  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `HIT`
  * Other Info: ``


Instances: 4

### Solution

Validate that the response does not contain sensitive, personal or user-specific information. If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:
Cache-Control: no-cache, no-store, must-revalidate, private
Pragma: no-cache
Expires: 0
This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.

### Reference


* [ https://datatracker.ietf.org/doc/html/rfc7234 ](https://datatracker.ietf.org/doc/html/rfc7234)
* [ https://datatracker.ietf.org/doc/html/rfc7231 ](https://datatracker.ietf.org/doc/html/rfc7231)
* [ https://www.rfc-editor.org/rfc/rfc9110.html ](https://www.rfc-editor.org/rfc/rfc9110.html)


#### CWE Id: [ 525 ](https://cwe.mitre.org/data/definitions/525.html)


#### Source ID: 3

### [ Session Management Response Identified ](https://www.zaproxy.org/docs/alerts/10112/)



##### Informational (Medium)

### Description

The given response has been identified as containing a session management token. The 'Other Info' field contains a set of header tokens that can be used in the Header Based Session Management Method. If the request is in a context which has a Session Management Method set to "Auto-Detect" then this rule will change the session management to use the tokens identified.

* URL: https://stats.csdiilit.com/

  * Method: `GET`
  * Parameter: `GAESA`
  * Attack: ``
  * Evidence: `GAESA`
  * Other Info: `cookie:GAESA`
* URL: https://stats.csdiilit.com/

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Felo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Felo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2501&elo_max=3000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&elo_min=2501&elo_max=3000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmax=100000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=100000&max=125000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=125000&max=150000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=150000&max=175000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=175000&max=200000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1501&elo_max=2000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=1501&elo_max=2000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&elo_min=2501&elo_max=3000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=200000&max=225000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=225000&max=250000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=1001&elo_max=1500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=2001&elo_max=2500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=250000&max=275000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_max=1000&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_max=1000&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_min=1001&elo_max=1500&limit=5000&offset=0

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/by_value%3Fmin=275000&max=300000&elo_min=2001&elo_max=2500&limit=5000&offset=0&role=draft_prospect

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpo&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAGZydEzA&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAGZydEzAgEsQCjFx&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoAYmOVUhA&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpojpTaPGXa&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=CgBlTvpoPqTfBRByyHlpRBJs&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIk&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkDyomvtdK&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkhmHhseKB&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=MpTqSjIkVvjPSGHe&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXu&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXuFwdlCpWZ&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=WtXxKkXuFwdlCpWZksHenaTyekjbtlIDriqHeqSlPHZVtRWzZMgDGCXyMgQMjzSyHseFSOilFKDvcQNKOIiHKMMdvqUgTyTBALnEEAgmpzBimfUPxwpzDXjl&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=ZmJRRbjk&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/api/players/search%3Fq=ZmJRRbjkMpTqSjIk&limit=20

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/auth/faceit/login

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/auth/me

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/info

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/robots.txt

  * Method: `GET`
  * Parameter: `GAESA`
  * Attack: ``
  * Evidence: `GAESA`
  * Other Info: `cookie:GAESA`
* URL: https://stats.csdiilit.com/search

  * Method: `GET`
  * Parameter: `sid`
  * Attack: ``
  * Evidence: `sid`
  * Other Info: `cookie:sid`
* URL: https://stats.csdiilit.com/sitemap.xml

  * Method: `GET`
  * Parameter: `GAESA`
  * Attack: ``
  * Evidence: `GAESA`
  * Other Info: `cookie:GAESA`
* URL: https://stats.csdiilit.com/

  * Method: `GET`
  * Parameter: `GAESA`
  * Attack: ``
  * Evidence: `GAESA`
  * Other Info: `cookie:GAESA`


Instances: 82

### Solution

This is an informational alert rather than a vulnerability and so there is nothing to fix.

### Reference


* [ https://www.zaproxy.org/docs/desktop/addons/authentication-helper/session-mgmt-id/ ](https://www.zaproxy.org/docs/desktop/addons/authentication-helper/session-mgmt-id/)



#### Source ID: 3


