# <img src="https://www.usac.org/wp-includes/images/w-logo-blue-white-bg.png" alt="USAC logo" width="28" height="28"> USAC: Universal API

USAC Open Data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uSAC/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://opendata.usac.org
- **Vendor API docs:** https://dev.socrata.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Datasets](actions/list-datasets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAC/latest/actions/list-datasets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Data](actions/get-data.md) | GET |  |
| [Get Data Count](actions/get-data-count.md) | GET |  |
| [List Dataset Categories](actions/list-dataset-categories.md) | GET |  |
| [List Datasets](actions/list-datasets.md) | GET |  |

