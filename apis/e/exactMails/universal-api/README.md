# <img src="https://images.mindcloud.co/apps/icons/exact-mails_1775824659745.png" alt="Exact Mails logo" width="28" height="28"> Exact Mails: Universal API

Find and verify professional email addresses

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/exactMails/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://exactmails.com
- **Vendor API docs:** https://exactmail-dashboard.vercel.app/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exactMails/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Exact Mails. |

