# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-13-as-14_1776106008698.png" alt="SurveyCTO logo" width="28" height="28"> SurveyCTO: Universal API

Collect, manage, and export survey and field data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/surveyCTO/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.surveycto.com
- **Vendor API docs:** https://developer.surveycto.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Datasets](actions/list-datasets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveyCTO/latest/actions/list-datasets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves all available datasets from SurveyCTO. |

