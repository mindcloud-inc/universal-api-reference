# <img src="https://images.mindcloud.co/apps/icons/captcha_1776710648332.png" alt="2Captcha logo" width="28" height="28"> 2Captcha: Universal API

2Captcha solves CAPTCHA challenges through API v2 task creation, polling, balance, and result reporting endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/captcha/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://2captcha.com
- **Vendor API docs:** https://2captcha.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captcha/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves your current 2Captcha account balance. |

### Captcha Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Amazon WAF Task Proxyless](actions/create-amazon-waf-task-proxyless.md) | POST | Creates a proxyless Amazon WAF captcha task in 2Captcha. |
| [Create Amazon WAF Task With Proxy](actions/create-amazon-waf-task-with-proxy.md) | POST | Creates a proxied Amazon WAF captcha task in 2Captcha. |
| [Create Arkose FunCaptcha Task Proxyless](actions/create-arkose-fun-captcha-task-proxyless.md) | POST | Creates a proxyless Arkose FunCaptcha task in 2Captcha. |
| [Create Arkose FunCaptcha Task With Proxy](actions/create-arkose-fun-captcha-task-with-proxy.md) | POST | Creates a proxied Arkose FunCaptcha task in 2Captcha. |
| [Create ATB Captcha Task Proxyless](actions/create-atb-captcha-task-proxyless.md) | POST | Creates a proxyless ATB captcha task in 2Captcha. |
| [Create ATB Captcha Task With Proxy](actions/create-atb-captcha-task-with-proxy.md) | POST | Creates a proxied ATB captcha task in 2Captcha. |
| [Create CaptchaFox Task](actions/create-captcha-fox-task.md) | POST | Creates a CaptchaFox captcha task in 2Captcha. |
| [Create Capy Puzzle Task Proxyless](actions/create-capy-puzzle-task-proxyless.md) | POST | Creates a proxyless Capy Puzzle task in 2Captcha. |
| [Create Capy Puzzle Task With Proxy](actions/create-capy-puzzle-task-with-proxy.md) | POST | Creates a proxied Capy Puzzle task in 2Captcha. |
| [Create Cloudflare Turnstile Task Proxyless](actions/create-cloudflare-turnstile-task-proxyless.md) | POST | Creates a proxyless Cloudflare Turnstile task in 2Captcha. |
| [Create Cloudflare Turnstile Task With Proxy](actions/create-cloudflare-turnstile-task-with-proxy.md) | POST | Creates a proxied Cloudflare Turnstile task in 2Captcha. |
| [Create CutCaptcha Task Proxyless](actions/create-cut-captcha-task-proxyless.md) | POST | Creates a proxyless CutCaptcha task in 2Captcha. |
| [Create CutCaptcha Task With Proxy](actions/create-cut-captcha-task-with-proxy.md) | POST | Creates a proxied CutCaptcha task in 2Captcha. |
| [Create DataDome Slider Task](actions/create-data-dome-slider-task.md) | POST | Creates a DataDome slider captcha task in 2Captcha. |
| [Create Friendly Captcha Task Proxyless](actions/create-friendly-captcha-task-proxyless.md) | POST | Creates a proxyless Friendly Captcha task in 2Captcha. |
| [Create Friendly Captcha Task With Proxy](actions/create-friendly-captcha-task-with-proxy.md) | POST | Creates a proxied Friendly Captcha task in 2Captcha. |
| [Create GeeTest Task Proxyless](actions/create-gee-test-task-proxyless.md) | POST | Creates a proxyless GeeTest task in 2Captcha. |
| [Create GeeTest Task With Proxy](actions/create-gee-test-task-with-proxy.md) | POST | Creates a proxied GeeTest task in 2Captcha. |
| [Create Image To Text Task](actions/create-image-to-text-task.md) | POST | Creates an image-to-text captcha task in 2Captcha. |
| [Create KeyCaptcha Task Proxyless](actions/create-key-captcha-task-proxyless.md) | POST | Creates a proxyless KeyCaptcha task in 2Captcha. |
| [Create KeyCaptcha Task With Proxy](actions/create-key-captcha-task-with-proxy.md) | POST | Creates a proxied KeyCaptcha task in 2Captcha. |
| [Create Lemin Task Proxyless](actions/create-lemin-task-proxyless.md) | POST | Creates a proxyless Lemin captcha task in 2Captcha. |
| [Create Lemin Task With Proxy](actions/create-lemin-task-with-proxy.md) | POST | Creates a proxied Lemin captcha task in 2Captcha. |
| [Create MTCaptcha Task Proxyless](actions/create-mt-captcha-task-proxyless.md) | POST | Creates a proxyless MTCaptcha task in 2Captcha. |
| [Create MTCaptcha Task With Proxy](actions/create-mt-captcha-task-with-proxy.md) | POST | Creates a proxied MTCaptcha task in 2Captcha. |
| [Create Prosopo Procaptcha Task Proxyless](actions/create-prosopo-procaptcha-task-proxyless.md) | POST | Creates a proxyless Prosopo Procaptcha task in 2Captcha. |
| [Create Prosopo Procaptcha Task With Proxy](actions/create-prosopo-procaptcha-task-with-proxy.md) | POST | Creates a proxied Prosopo Procaptcha task in 2Captcha. |
| [Create reCAPTCHA V2 Enterprise Task Proxyless](actions/create-re-captchav2-enterprise-task-proxyless.md) | POST | Creates a proxyless reCAPTCHA v2 Enterprise task in 2Captcha. |
| [Create reCAPTCHA V2 Enterprise Task With Proxy](actions/create-re-captchav2-enterprise-task-with-proxy.md) | POST | Creates a proxied reCAPTCHA v2 Enterprise task in 2Captcha. |
| [Create reCAPTCHA V2 Task Proxyless](actions/create-re-captchav2-task-proxyless.md) | POST | Creates a proxyless reCAPTCHA v2 task in 2Captcha. |
| [Create reCAPTCHA V2 Task With Proxy](actions/create-re-captchav2-task-with-proxy.md) | POST | Creates a proxied reCAPTCHA v2 task in 2Captcha. |
| [Create reCAPTCHA V3 Task Proxyless](actions/create-re-captchav3-task-proxyless.md) | POST | Creates a proxyless reCAPTCHA v3 task in 2Captcha. |
| [Create Rotate Task](actions/create-rotate-task.md) | POST | Creates a rotate captcha task in 2Captcha. |
| [Create Tencent Captcha Task Proxyless](actions/create-tencent-captcha-task-proxyless.md) | POST | Creates a proxyless Tencent captcha task in 2Captcha. |
| [Create Tencent Captcha Task With Proxy](actions/create-tencent-captcha-task-with-proxy.md) | POST | Creates a proxied Tencent captcha task in 2Captcha. |
| [Create Text Captcha Task](actions/create-text-captcha-task.md) | POST | Creates a text captcha task in 2Captcha. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Result](actions/get-task-result.md) | GET | Retrieves the current result for a 2Captcha task. |
| [Report Correct](actions/report-correct.md) | PUT | Marks a 2Captcha task result as correct. |
| [Report Incorrect](actions/report-incorrect.md) | PUT | Marks a 2Captcha task result as incorrect. |

