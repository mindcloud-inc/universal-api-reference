# <img src="https://images.mindcloud.co/apps/icons/icon_1774375183617.png" alt="Linkly logo" width="28" height="28"> Linkly: Universal API

Create, manage, and track branded short links with click analytics, redirects, and QR codes.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/linkly/latest
- **Category:** Marketing
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://linklyhq.com
- **Vendor API docs:** https://linklyhq.com/support/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Links](actions/list-links.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkly/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Click

| Action | Method | Description |
| --- | --- | --- |
| [Get Click Analytics](actions/get-click-analytics.md) | GET | Retrieves click analytics from Linkly. |

### Click Counter

| Action | Method | Description |
| --- | --- | --- |
| [Get Click Counts Grouped By Dimension](actions/get-click-counts-grouped-by-dimension.md) | GET | Retrieves click counts by dimension from Linkly. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Link](actions/create-link.md) | POST | Creates a new link in Linkly. |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes an existing link from Linkly. |
| [Export Links](actions/export-links.md) | GET | Retrieves a link export from Linkly. |
| [Get Link](actions/get-link.md) | GET | Retrieves a link from Linkly. |
| [List Links](actions/list-links.md) | GET | Retrieves links from Linkly. |
| [Update Link](actions/update-link.md) | PUT | Updates an existing link in Linkly. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Linkly. |

