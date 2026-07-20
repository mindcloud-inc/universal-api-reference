# <img src="https://images.mindcloud.co/apps/icons/dyna-pictures_1774629435593.png" alt="DynaPictures logo" width="28" height="28"> DynaPictures: Universal API

Generate and manage dynamic images, templates, and media assets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dynaPictures/latest
- **Category:** Marketing
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dynapictures.com
- **Vendor API docs:** https://dynapictures.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Delete Asset](actions/delete-asset.md) | DELETE | Deletes an asset from a DynaPictures workspace. |
| [Get Asset](actions/get-asset.md) | GET | Retrieves an asset from a DynaPictures workspace by ID. |
| [List Assets](actions/list-assets.md) | GET | Retrieves assets from a DynaPictures workspace. |
| [Update Asset](actions/update-asset.md) | PUT | Updates an asset in a DynaPictures workspace. |
| [Upload Asset](actions/upload-asset.md) | POST | Uploads an asset to a DynaPictures workspace. |

### Generated Image

| Action | Method | Description |
| --- | --- | --- |
| [Delete Generated Image](actions/delete-generated-image.md) | DELETE | Deletes a generated image from DynaPictures. |
| [Generate Image](actions/generate-image.md) | POST | Creates an image from a DynaPictures template. |
| [Generate Multipage Images](actions/generate-multipage-images.md) | POST | Creates images from a multipage DynaPictures template. |

### Generated Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Generate Multipage PDF](actions/generate-multipage-pdf.md) | POST | Creates a PDF from a multipage DynaPictures template. |
| [Generate Template PDF](actions/generate-template-pdf.md) | POST | Creates a PDF from a DynaPictures template. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from DynaPictures by UID. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from DynaPictures. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe Webhook](actions/subscribe-webhook.md) | POST | Creates a webhook subscription in DynaPictures. |
| [Unsubscribe Webhook](actions/unsubscribe-webhook.md) | DELETE | Deletes a webhook subscription from DynaPictures. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a workspace in DynaPictures. |
| [Delete Workspace](actions/delete-workspace.md) | DELETE | Deletes an existing workspace from DynaPictures. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from DynaPictures. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates an existing workspace in DynaPictures. |

