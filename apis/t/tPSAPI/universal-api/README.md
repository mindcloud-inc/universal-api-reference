# <img src="https://images.mindcloud.co/apps/icons/images-5_1775073770564.png" alt="TPS API logo" width="28" height="28"> TPS API: Universal API

Screen phone numbers against TPS and CTPS suppression lists

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tPSAPI/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tpsapi.com
- **Vendor API docs:** https://tpsapi.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Screen Phone Numbers](actions/screen-phone-numbers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tPSAPI/latest/actions/screen-phone-numbers?connectionId=$CONNECTION_ID&phoneNumbers=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Screen Phone Numbers](actions/screen-phone-numbers.md) | GET | Screens phone numbers against TPS and CTPS lists in TPS API. |

