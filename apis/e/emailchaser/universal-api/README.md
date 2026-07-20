# <img src="https://images.mindcloud.co/apps/icons/favicon-run-emailchaser-com-48x48-1_1776265724770.png" alt="Emailchaser logo" width="28" height="28"> Emailchaser: Universal API

Manage campaigns and leads with Emailchaser

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/emailchaser/latest
- **Category:** Marketing
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.emailchaser.com
- **Vendor API docs:** https://run.emailchaser.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Campaigns](actions/list-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailchaser/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET |  |

