# <img src="https://images.mindcloud.co/apps/icons/veriphone_1774540734127.png" alt="Veriphone logo" width="28" height="28"> Veriphone: Universal API

Validate phone numbers and look up carriers.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/veriphone/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://veriphone.io
- **Vendor API docs:** https://veriphone.io/docs/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Example Phone Number](actions/get-example-phone-number.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veriphone/latest/actions/get-example-phone-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Get Example Phone Number](actions/get-example-phone-number.md) | GET |  |
| [Validate Phone Number](actions/validate-phone-number.md) | GET |  |

