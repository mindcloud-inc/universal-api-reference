# 2Captcha: Native API Reference

A consolidated summary of 2Captcha's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://2captcha.com/api-docs
- **API base URL:** `https://api.2captcha.com`

## Authentication

### API Key

Use a 2Captcha API key. API v2 sends it as `clientKey` in each JSON request body.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://2captcha.com/api-docs/quick-start)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Amazon WAF Task Proxyless](actions/create-amazon-waf-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/amazon-aws-waf-captcha) |
| [Create Amazon WAF Task With Proxy](actions/create-amazon-waf-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/amazon-aws-waf-captcha) |
| [Create Arkose FunCaptcha Task Proxyless](actions/create-arkose-fun-captcha-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/arkoselabs-funcaptcha) |
| [Create Arkose FunCaptcha Task With Proxy](actions/create-arkose-fun-captcha-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/arkoselabs-funcaptcha) |
| [Create ATB Captcha Task Proxyless](actions/create-atb-captcha-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/atb-captcha) |
| [Create ATB Captcha Task With Proxy](actions/create-atb-captcha-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/atb-captcha) |
| [Create CaptchaFox Task](actions/create-captcha-fox-task.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/captchafox) |
| [Create Capy Puzzle Task Proxyless](actions/create-capy-puzzle-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/capy-puzzle-captcha) |
| [Create Capy Puzzle Task With Proxy](actions/create-capy-puzzle-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/capy-puzzle-captcha) |
| [Create Cloudflare Turnstile Task Proxyless](actions/create-cloudflare-turnstile-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/cloudflare-turnstile) |
| [Create Cloudflare Turnstile Task With Proxy](actions/create-cloudflare-turnstile-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/cloudflare-turnstile) |
| [Create CutCaptcha Task Proxyless](actions/create-cut-captcha-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/cutcaptcha) |
| [Create CutCaptcha Task With Proxy](actions/create-cut-captcha-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/cutcaptcha) |
| [Create DataDome Slider Task](actions/create-data-dome-slider-task.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/datadome-slider-captcha) |
| [Create Friendly Captcha Task Proxyless](actions/create-friendly-captcha-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/friendly-captcha) |
| [Create Friendly Captcha Task With Proxy](actions/create-friendly-captcha-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/friendly-captcha) |
| [Create GeeTest Task Proxyless](actions/create-gee-test-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/geetest) |
| [Create GeeTest Task With Proxy](actions/create-gee-test-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/geetest) |
| [Create Image To Text Task](actions/create-image-to-text-task.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/normal-captcha) |
| [Create KeyCaptcha Task Proxyless](actions/create-key-captcha-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/keycaptcha) |
| [Create KeyCaptcha Task With Proxy](actions/create-key-captcha-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/keycaptcha) |
| [Create Lemin Task Proxyless](actions/create-lemin-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/lemin) |
| [Create Lemin Task With Proxy](actions/create-lemin-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/lemin) |
| [Create MTCaptcha Task Proxyless](actions/create-mt-captcha-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/mtcaptcha) |
| [Create MTCaptcha Task With Proxy](actions/create-mt-captcha-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/mtcaptcha) |
| [Create Prosopo Procaptcha Task Proxyless](actions/create-prosopo-procaptcha-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/prosopo-procaptcha) |
| [Create Prosopo Procaptcha Task With Proxy](actions/create-prosopo-procaptcha-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/prosopo-procaptcha) |
| [Create reCAPTCHA V2 Enterprise Task Proxyless](actions/create-re-captchav2-enterprise-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/recaptcha-v2-enterprise) |
| [Create reCAPTCHA V2 Enterprise Task With Proxy](actions/create-re-captchav2-enterprise-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/recaptcha-v2-enterprise) |
| [Create reCAPTCHA V2 Task Proxyless](actions/create-re-captchav2-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/recaptcha-v2) |
| [Create reCAPTCHA V2 Task With Proxy](actions/create-re-captchav2-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/recaptcha-v2) |
| [Create reCAPTCHA V3 Task Proxyless](actions/create-re-captchav3-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/recaptcha-v3) |
| [Create Rotate Task](actions/create-rotate-task.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/rotate) |
| [Create Tencent Captcha Task Proxyless](actions/create-tencent-captcha-task-proxyless.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/tencent) |
| [Create Tencent Captcha Task With Proxy](actions/create-tencent-captcha-task-with-proxy.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/tencent) |
| [Create Text Captcha Task](actions/create-text-captcha-task.md) | `POST /createTask` | [docs](https://2captcha.com/api-docs/text) |
| [Get Balance](actions/get-balance.md) | `POST /getBalance` | [docs](https://2captcha.com/api-docs/get-balance) |
| [Get Task Result](actions/get-task-result.md) | `POST /getTaskResult` | [docs](https://2captcha.com/api-docs/get-task-result) |
| [Report Correct](actions/report-correct.md) | `POST /reportCorrect` | [docs](https://2captcha.com/api-docs/report-correct) |
| [Report Incorrect](actions/report-incorrect.md) | `POST /reportIncorrect` | [docs](https://2captcha.com/api-docs/report-incorrect) |
