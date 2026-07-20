# <img src="https://images.mindcloud.co/apps/icons/switchyio_1774466854276.png" alt="Switchy.io logo" width="28" height="28"> Switchy.io: Universal API

Create branded links, manage smart pages, and track clicks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/switchyio/latest
- **Category:** Marketing
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://switchy.io
- **Vendor API docs:** https://developers.switchy.io/docs/overview/index

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Count Workspaces](actions/count-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/count-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain](actions/get-domain.md) | GET | Retrieves a domain from Switchy.io by name and owner ID. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from Switchy.io. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a folder from Switchy.io by ID. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from Switchy.io. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Delete Links](actions/bulk-delete-links.md) | DELETE | Deletes existing links from Switchy.io by domain and IDs. |
| [Bulk Update Links](actions/bulk-update-links.md) | PUT | Updates existing links in Switchy.io by domain and IDs. |
| [Create Link](actions/create-link.md) | POST | Creates a new link in Switchy.io. |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes an existing link from Switchy.io by domain and ID. |
| [Get Link](actions/get-link.md) | GET | Retrieves a link from Switchy.io by domain and ID. |
| [List Links](actions/list-links.md) | GET | Retrieves links from Switchy.io. |
| [Update Link](actions/update-link.md) | PUT | Updates an existing link in Switchy.io. |

### Link Script

| Action | Method | Description |
| --- | --- | --- |
| [Get Link Script](actions/get-link-script.md) | GET | Retrieves a link script from Switchy.io by ID. |
| [List Link Scripts](actions/list-link-scripts.md) | GET | Retrieves link scripts from Switchy.io. |

### Pixel

| Action | Method | Description |
| --- | --- | --- |
| [Get Pixel](actions/get-pixel.md) | GET | Retrieves a pixel from Switchy.io by ID. |
| [List Pixels](actions/list-pixels.md) | GET | Retrieves pixels from Switchy.io. |

### Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Token](actions/get-token.md) | GET | Retrieves a token from Switchy.io by UID. |
| [List Tokens](actions/list-tokens.md) | GET | Retrieves tokens from Switchy.io. |

### Utm Template

| Action | Method | Description |
| --- | --- | --- |
| [Get UTM Template](actions/get-utm-template.md) | GET | Retrieves a UTM template from Switchy.io by ID. |
| [List UTM Templates](actions/list-utm-templates.md) | GET | Retrieves UTM templates from Switchy.io. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Count Workspaces](actions/count-workspaces.md) | GET | Retrieves the workspace count from Switchy.io. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Switchy.io by ID. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Switchy.io. |

