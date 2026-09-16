# <img src="https://images.mindcloud.co/apps/icons/bar-tender_1784239365989.png" alt="BarTender logo" width="28" height="28"> BarTender: Universal API

Run BarTender Cloud automation scripts and print workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/barTender/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bartendersoftware.com/product/cloud
- **Vendor API docs:** https://help.seagullscientific.com/BarTenderCloud/Help/en/Content/API/API_Doc_BTC_API_Documentation_LP.htm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/barTender/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user profile from BarTender Cloud. |

