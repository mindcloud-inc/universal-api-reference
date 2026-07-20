# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-16-as-15_1776364191196.png" alt="Anyware Services logo" width="28" height="28"> Anyware Services: Universal API

Import XML content into Ametys CMS sites

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/anywareServices/latest
- **Category:** Website & App Building / CMS
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ametys.org
- **Vendor API docs:** https://docs.ametys.org/fr/plugins/content-io/v1/manuel-utilisateur.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Import Content At Root](actions/import-content-at-root.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anywareServices/latest/actions/import-content-at-root" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "site": "string",
  "lang": "string",
  "content": "string"
}'
```

## Actions (2)

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Import Content At Root](actions/import-content-at-root.md) | POST | Creates a page and imported content at the site root in Anyware Services. |
| [Import Content Under Parent Path](actions/import-content-under-parent-path.md) | POST | Creates a page and imported content under a parent path in Anyware Services. |

