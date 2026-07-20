# <img src="https://images.mindcloud.co/apps/icons/page-x_1775668625681.png" alt="PageX logo" width="28" height="28"> PageX: Universal API

PageX is a CRM and digital-business platform for managing leads, landing pages, and online courses.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pageX/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pagexcrm.com
- **Vendor API docs:** https://rapidapi.com/thunderhurt/api/pagexcrm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Add Lead](actions/add-lead.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pageX/latest/actions/add-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

## Actions (1)

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Add Lead](actions/add-lead.md) | POST |  |

