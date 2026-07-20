# <img src="https://images.mindcloud.co/apps/icons/688202f83990f13bdb4e01a7-n2b-256x256_1775138794651.png" alt="no2bounce logo" width="28" height="28"> no2bounce: Universal API

Validate email lists with no2bounce bulk verification jobs and retrieve validation status results for deliverability workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/no2bounce/latest
- **Category:** Marketing
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.no2bounce.com
- **Vendor API docs:** https://www.no2bounce.com/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Bulk Validation Status](actions/get-bulk-validation-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/no2bounce/latest/actions/get-bulk-validation-status?connectionId=$CONNECTION_ID&trackingId=Paste%20the%20tracking%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Validation Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Validation Status](actions/get-bulk-validation-status.md) | GET | Retrieves bulk validation status from no2bounce by tracking ID. |
| [Submit Bulk Validation](actions/submit-bulk-validation.md) | POST | Creates a bulk validation job in no2bounce. |

