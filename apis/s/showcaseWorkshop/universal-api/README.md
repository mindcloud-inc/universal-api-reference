# <img src="https://images.mindcloud.co/apps/icons/favicon-github-com-48x48_1777641516265.png" alt="Showcase Workshop logo" width="28" height="28"> Showcase Workshop: Universal API

Showcase Workshop is a presentation builder and distribution platform for managing sales and marketing collateral, collecting Showcase form data, and retrieving data submitted from Showcase content.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/showcaseWorkshop/latest
- **Category:** Marketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.showcaseworkshop.com
- **Vendor API docs:** https://github.com/ShowcaseSoftwareLtd/showcase-workshop-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Data](actions/list-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/list-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Data

| Action | Method | Description |
| --- | --- | --- |
| [Add Data](actions/add-data.md) | POST | Creates a data item in Showcase Workshop. |
| [Delete Data](actions/delete-data.md) | DELETE | Deletes a data item from Showcase Workshop. |
| [Get Data](actions/get-data.md) | GET | Retrieves a data item from Showcase Workshop. |
| [List Data](actions/list-data.md) | GET | Retrieves data items from Showcase Workshop. |

