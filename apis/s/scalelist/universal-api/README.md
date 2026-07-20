# <img src="https://images.mindcloud.co/apps/icons/scalelist_1774977566933.png" alt="Scalelist logo" width="28" height="28"> Scalelist: Universal API

Find verified work emails and mobile numbers for prospects

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scalelist/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scalelist.com
- **Vendor API docs:** https://app.scalelist.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Find Email](actions/find-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scalelist/latest/actions/find-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Find Email](actions/find-email.md) | GET | Finds a contact email in Scalelist. |
| [Find Phone](actions/find-phone.md) | GET | Finds a contact phone number in Scalelist. |

