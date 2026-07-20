# <img src="https://images.mindcloud.co/apps/icons/dynamic-mockups_1775154113704.jpeg" alt="Dynamic Mockups logo" width="28" height="28"> Dynamic Mockups: Universal API

Dynamic Mockups generates product mockups and print assets from templates and PSD files via API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dynamicMockups/latest
- **Category:** Commerce
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dynamicmockups.com
- **Vendor API docs:** https://docs.dynamicmockups.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Collections](actions/list-collections.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Bulk Renders](actions/create-bulk-renders.md) | POST | Creates bulk renders from a Dynamic Mockups collection. |
| [Create Mockup Render](actions/create-mockup-render.md) | POST | Creates a mockup render in Dynamic Mockups. |
| [Delete PSD File](actions/delete-psd-file.md) | DELETE | Deletes a PSD file from Dynamic Mockups. |
| [Export Print Files](actions/export-print-files.md) | POST | Exports print files from a Dynamic Mockups mockup. |
| [Get Mockup](actions/get-mockup.md) | GET | Retrieves a mockup from Dynamic Mockups by UUID. |
| [List Mockups](actions/list-mockups.md) | GET | Retrieves your mockups from Dynamic Mockups. |
| [Render Multiple Mockups](actions/render-multiple-mockups.md) | POST | Creates multiple mockup renders in Dynamic Mockups. |
| [Upload PSD File](actions/upload-psd-file.md) | POST | Uploads a PSD file to Dynamic Mockups. |

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [List Catalogs](actions/list-catalogs.md) | GET | Retrieves your catalogs from Dynamic Mockups. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Dynamic Mockups. |
| [List Collections](actions/list-collections.md) | GET | Retrieves your collections from Dynamic Mockups. |

