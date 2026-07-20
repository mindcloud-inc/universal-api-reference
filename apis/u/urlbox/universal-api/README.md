# <img src="https://images.mindcloud.co/apps/icons/urlbox_1774038977196.png" alt="Urlbox logo" width="28" height="28"> Urlbox: Universal API

Capture website screenshots, PDFs, videos, metadata, and HTML

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/urlbox/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://urlbox.com
- **Vendor API docs:** https://urlbox.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Render Status](actions/check-render-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/check-render-status?connectionId=$CONNECTION_ID&renderId=250ea007-552c-4555-ba2b-ef1c73e18be2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Render

| Action | Method | Description |
| --- | --- | --- |
| [Check Render Status](actions/check-render-status.md) | GET | Retrieves the status of a render from Urlbox. |
| [Create Asynchronous Render](actions/create-asynchronous-render.md) | POST | Creates an asynchronous render in Urlbox. |
| [Create Synchronous Render](actions/create-synchronous-render.md) | POST | Creates a synchronous render in Urlbox. |

