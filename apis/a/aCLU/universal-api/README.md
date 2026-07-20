# <img src="https://images.mindcloud.co/apps/icons/a-clu_1776357935597.png" alt="ACLU logo" width="28" height="28"> ACLU: Universal API

ACLU update-app persistence probe

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aCLU/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.thetorturedatabase.org
- **Vendor API docs:** https://www.thetorturedatabase.org/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Node By NID](actions/get-node-by-nid.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aCLU/latest/actions/get-node-by-nid?connectionId=$CONNECTION_ID&nid=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [List Nodes By Type](actions/list-nodes-by-type.md) | GET | Retrieves Torture Database nodes by content type. |
| [Search Nodes](actions/search-nodes.md) | GET | Finds Torture Database nodes by keyword and filters. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Node By NID](actions/get-node-by-nid.md) | GET | Retrieves a Torture Database node by numeric ID. |

