# <img src="https://images.mindcloud.co/apps/icons/diabolocom-logo_1776944390959.jpeg" alt="Diabolocom logo" width="28" height="28"> Diabolocom: Universal API

Diabolocom AI APIs for submitting text and audio analysis jobs and retrieving asynchronous job results.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/diabolocom/latest
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.diabolocom.com/
- **Vendor API docs:** https://developer.diabolocom.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Job Status](actions/get-job-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diabolocom/latest/actions/get-job-status?connectionId=$CONNECTION_ID&jobId=job_123&expires=string&signature=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Contact Reason Job

| Action | Method | Description |
| --- | --- | --- |
| [Detect Contact Reason](actions/detect-contact-reason.md) | POST | Creates a contact reason detection job in Diabolocom. |

### Email Extraction Job

| Action | Method | Description |
| --- | --- | --- |
| [Extract Email Addresses](actions/extract-email-addresses.md) | POST | Creates an email address extraction job in Diabolocom. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Status](actions/get-job-status.md) | GET | Retrieves a task job status from Diabolocom. |

### Language Detection Job

| Action | Method | Description |
| --- | --- | --- |
| [Detect Languages Used](actions/detect-languages-used.md) | POST | Creates a language detection job in Diabolocom. |

### Location Extraction Job

| Action | Method | Description |
| --- | --- | --- |
| [Extract Locations](actions/extract-locations.md) | POST | Creates a location extraction job in Diabolocom. |

### Mail Tag Extraction Job

| Action | Method | Description |
| --- | --- | --- |
| [Extract Mail Tags](actions/extract-mail-tags.md) | POST | Creates a mail tag extraction job in Diabolocom. |

### Monetary Value Extraction Job

| Action | Method | Description |
| --- | --- | --- |
| [Extract Monetary Values](actions/extract-monetary-values.md) | POST | Creates a monetary value extraction job in Diabolocom. |

### Person Name Extraction Job

| Action | Method | Description |
| --- | --- | --- |
| [Extract Person Names](actions/extract-person-names.md) | POST | Creates a person name extraction job in Diabolocom. |

### Phone Number Extraction Job

| Action | Method | Description |
| --- | --- | --- |
| [Extract Phone Numbers](actions/extract-phone-numbers.md) | POST | Creates a phone number extraction job in Diabolocom. |

### Product Extraction Job

| Action | Method | Description |
| --- | --- | --- |
| [Extract Products](actions/extract-products.md) | POST | Creates a product extraction job in Diabolocom. |

### Question Answering Job

| Action | Method | Description |
| --- | --- | --- |
| [Answer Question](actions/answer-question.md) | POST | Creates a question answering job in Diabolocom. |

### Rating Estimation Job

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Rating](actions/estimate-rating.md) | POST | Creates a rating estimation job in Diabolocom. |

### Satisfaction Factors Job

| Action | Method | Description |
| --- | --- | --- |
| [Detect Satisfaction Factors](actions/detect-satisfaction-factors.md) | POST | Creates a satisfaction factor detection job in Diabolocom. |

### Touchpoint Extraction Job

| Action | Method | Description |
| --- | --- | --- |
| [Extract Touchpoints](actions/extract-touchpoints.md) | POST | Creates a touchpoint extraction job in Diabolocom. |

### Translation Job

| Action | Method | Description |
| --- | --- | --- |
| [Translate Text](actions/translate-text.md) | POST | Creates a text translation job in Diabolocom. |

