# <img src="https://images.mindcloud.co/apps/icons/t-pscheck_1776945993833.png" alt="TPSCheck logo" width="28" height="28"> TPSCheck: Universal API

Check TPS/CTPS status, validate phone numbers, and track credits

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tPSCheck/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tpscheck.uk/
- **Vendor API docs:** https://www.tpscheck.uk/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tPSCheck/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get credits](actions/get-credits.md) | GET |  |

### Phonecheckresult

| Action | Method | Description |
| --- | --- | --- |
| [Batch check phone numbers](actions/batch-check-phone-numbers.md) | GET |  |
| [Check phone number](actions/check-phone-number.md) | GET |  |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Check status](actions/check-status.md) | GET |  |

