# <img src="https://images.mindcloud.co/apps/icons/look-digital-signage_1774905394415.png" alt="Look Digital Signage logo" width="28" height="28"> Look Digital Signage: Universal API

Trigger preconfigured digital signage actions in Look CMS using a Look Action API key and per-action Action Links.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lookDigitalSignage/latest
- **Category:** Website & App Building / CMS
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lookdigitalsignage.com
- **Vendor API docs:** https://www.lookdigitalsignage.com/knowledge-base/actions

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Trigger Action](actions/trigger-action.md):

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lookDigitalSignage/latest/actions/trigger-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionLink": "https://...your-look-action-link..."
}'
```

## Actions (1)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Action](actions/trigger-action.md) | PUT | Triggers a configured action in Look Digital Signage. |

