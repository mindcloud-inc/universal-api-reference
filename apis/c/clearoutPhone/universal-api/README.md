# <img src="https://images.mindcloud.co/apps/icons/clearout-phone-3pjgxm_1774382877766.png" alt="ClearoutPhone logo" width="28" height="28"> ClearoutPhone: Universal API

Validate phone numbers worldwide and retrieve carrier, line type, location, and credit availability with the ClearoutPhone REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clearoutPhone/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://clearoutphone.io/
- **Vendor API docs:** https://docs.clearoutphone.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Available Credits](actions/get-available-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearoutPhone/latest/actions/get-available-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Bulk Validation Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Bulk Phone Number Validation](actions/create-bulk-phone-number-validation.md) | POST | Creates a bulk phone number validation job in ClearoutPhone. |

### Bulk Validation Result File

| Action | Method | Description |
| --- | --- | --- |
| [Download Bulk Phone Number Validation Result](actions/download-bulk-phone-number-validation-result.md) | GET | Retrieves the result of a bulk validation job from ClearoutPhone. |

### Bulk Validation Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Phone Number Validation Progress Status](actions/get-bulk-phone-number-validation-progress-status.md) | GET | Retrieves the progress status of a bulk validation job in ClearoutPhone. |

### Credits Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Available Credits](actions/get-available-credits.md) | GET | Retrieves the available credits from ClearoutPhone. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Validate Phone Number Instantly](actions/validate-phone-number-instantly.md) | GET | Retrieves instant validation details for a phone number from ClearoutPhone. |

