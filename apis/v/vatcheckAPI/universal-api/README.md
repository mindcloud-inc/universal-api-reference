# <img src="https://images.mindcloud.co/apps/icons/vatcheckapi_1778086074994.png" alt="VatcheckAPI logo" width="28" height="28"> VatcheckAPI: Universal API

VAT number validation and lookup API for checking VAT number format, checksum, registration details, and account quota status.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vatcheckAPI/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vatcheckapi.com/
- **Vendor API docs:** https://vatcheckapi.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Status](actions/check-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vatcheckAPI/latest/actions/check-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Quota Status

| Action | Method | Description |
| --- | --- | --- |
| [Check Status](actions/check-status.md) | GET | Retrieves the current quota status from VatcheckAPI. |

### Vat Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate VAT Number](actions/validate-vat-number.md) | GET | Validates a VAT number in VatcheckAPI. |

