# <img src="https://images.mindcloud.co/apps/icons/landingi_1773670528889.png" alt="Landingi logo" width="28" height="28"> Landingi: Universal API

Create and monitor programmatic landing page processes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/landingi/latest
- **Category:** Marketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://landingi.com/
- **Vendor API docs:** https://api.landingi.com/v2/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Programmatic Processes](actions/list-programmatic-processes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landingi/latest/actions/list-programmatic-processes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Programmatic Landing Page

| Action | Method | Description |
| --- | --- | --- |
| [List Landing Pages for Programmatic Process](actions/list-landing-pages-for-programmatic-process.md) | GET | Retrieves landing pages for a Landingi programmatic process. |

### Programmatic Process

| Action | Method | Description |
| --- | --- | --- |
| [Get Programmatic Process](actions/get-programmatic-process.md) | GET | Retrieves a programmatic process from Landingi by UUID. |
| [List Programmatic Processes](actions/list-programmatic-processes.md) | GET | Retrieves programmatic landing page processes from Landingi. |
| [Start Programmatic Process](actions/start-programmatic-process.md) | POST | Starts a programmatic landing page process in Landingi. |

