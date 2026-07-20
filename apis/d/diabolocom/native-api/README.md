# Diabolocom: Native API Reference

A consolidated summary of Diabolocom's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://developer.diabolocom.com/
- **API base URL:** `https://api.diabolocom.ai`

## Authentication

### API Key

Use a Diabolocom AI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.diabolocom.com/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Answer Question](actions/answer-question.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Detect Contact Reason](actions/detect-contact-reason.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Detect Languages Used](actions/detect-languages-used.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Detect Satisfaction Factors](actions/detect-satisfaction-factors.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Estimate Rating](actions/estimate-rating.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Extract Email Addresses](actions/extract-email-addresses.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Extract Locations](actions/extract-locations.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Extract Mail Tags](actions/extract-mail-tags.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Extract Monetary Values](actions/extract-monetary-values.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Extract Person Names](actions/extract-person-names.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Extract Phone Numbers](actions/extract-phone-numbers.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Extract Products](actions/extract-products.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Extract Touchpoints](actions/extract-touchpoints.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Get Job Status](actions/get-job-status.md) | `GET https://execute.diabolocom.ai/api/job/status/:jobId` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
| [Translate Text](actions/translate-text.md) | `POST /api/job/text-tasks` | [docs](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest) |
