# <img src="https://images.mindcloud.co/apps/icons/orshot_1775502551687.png" alt="Orshot logo" width="28" height="28"> Orshot: Universal API

Generate renders, manage templates, and manage workspace assets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/orshot/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://orshot.com
- **Vendor API docs:** https://orshot.com/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile and Workspaces](actions/get-profile-and-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-profile-and-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Add Brand Color](actions/add-brand-color.md) | POST |  |
| [Delete Brand Asset Image](actions/delete-brand-asset-image.md) | DELETE |  |
| [Delete Brand Color](actions/delete-brand-color.md) | DELETE |  |
| [Delete Brand Video](actions/delete-brand-video.md) | DELETE |  |
| [Get Brand Asset Images](actions/get-brand-asset-images.md) | GET |  |
| [Get Brand Colors](actions/get-brand-colors.md) | GET |  |
| [Get Brand Fonts](actions/get-brand-fonts.md) | GET |  |
| [Get Brand Videos](actions/get-brand-videos.md) | GET |  |
| [Update Brand Asset Image Tags](actions/update-brand-asset-image-tags.md) | PUT |  |
| [Update Brand Color Tags](actions/update-brand-color-tags.md) | PUT |  |
| [Update Brand Video Tags](actions/update-brand-video-tags.md) | PUT |  |
| [Upload Brand Asset Image](actions/upload-brand-asset-image.md) | POST |  |
| [Upload Brand Video](actions/upload-brand-video.md) | POST |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Generate Signed URL](actions/generate-signed-url.md) | POST |  |
| [Render from a Utility Template](actions/render-from-a-utility-template.md) | POST |  |
| [Render from Studio Template](actions/render-from-studio-template.md) | POST |  |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Delete Studio Template](actions/delete-studio-template.md) | DELETE |  |
| [Get All Studio Templates](actions/get-all-studio-templates.md) | GET |  |
| [Get Studio Template](actions/get-studio-template.md) | GET |  |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile and Workspaces](actions/get-profile-and-workspaces.md) | GET |  |

