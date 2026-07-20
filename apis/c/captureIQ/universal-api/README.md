# <img src="https://images.mindcloud.co/apps/icons/images_1775056119682.png" alt="CaptureIQ logo" width="28" height="28"> CaptureIQ: Universal API

Build forms, collect responses, and analyze submission insights

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/captureIQ/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.captureiq.ai
- **Vendor API docs:** https://help.captureiq.ai/api-reference/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate API Key](actions/validate-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captureIQ/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Validate API Key](actions/validate-api-key.md) | GET | Retrieves API key validation status from CaptureIQ. |

### Form Submission

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Recent Form Submission](actions/retrieve-recent-form-submission.md) | GET | Retrieves a recent form submission from CaptureIQ. |

