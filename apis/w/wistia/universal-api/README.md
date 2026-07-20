# <img src="https://images.mindcloud.co/apps/icons/images-1_1773760870917.png" alt="Wistia logo" width="28" height="28"> Wistia: Universal API

Manage Wistia videos, folders, captions, and analytics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wistia/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wistia.com
- **Vendor API docs:** https://docs.wistia.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Account](actions/get-current-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Background Job

| Action | Method | Description |
| --- | --- | --- |
| [Archive Media](actions/archive-media.md) | PUT | Archives one or more media items in Wistia. |
| [Move Media](actions/move-media.md) | PUT | Moves media to another Wistia folder or subfolder. |
| [Restore Media](actions/restore-media.md) | PUT | Restores archived media to your Wistia account. |
| [Show Background Job Status](actions/show-background-job-status.md) | GET | Retrieves the status of a Wistia background job. |

### Caption

| Action | Method | Description |
| --- | --- | --- |
| [Create Captions](actions/create-captions.md) | POST | Adds captions to a Wistia media item. |
| [Delete Captions](actions/delete-captions.md) | DELETE | Deletes captions for a Wistia media language. |
| [List Captions by Media](actions/list-captions-by-media.md) | GET | Retrieves captions for a Wistia media item. |
| [Show Captions](actions/show-captions.md) | GET | Retrieves captions for a Wistia media in one language. |
| [Update Captions](actions/update-captions.md) | PUT | Updates captions for a Wistia media language. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account](actions/get-current-account.md) | GET | Retrieves the current Wistia account details. |

### Customization

| Action | Method | Description |
| --- | --- | --- |
| [Show Customizations](actions/show-customizations.md) | GET | Retrieves customizations for a Wistia media item. |
| [Update Customizations](actions/update-customizations.md) | PUT | Updates customizations for a Wistia media item. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Wistia. |
| [Create Subfolder](actions/create-subfolder.md) | POST | Creates a new subfolder in a Wistia folder. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes an existing folder from Wistia. |
| [Delete Subfolder](actions/delete-subfolder.md) | DELETE | Deletes a subfolder from a Wistia folder. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a single folder from Wistia. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from the Wistia account. |
| [List Subfolders](actions/list-subfolders.md) | GET | Retrieves subfolders from a Wistia folder. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in Wistia. |
| [Update Subfolder](actions/update-subfolder.md) | PUT | Updates an existing subfolder in Wistia. |

### Media

| Action | Method | Description |
| --- | --- | --- |
| [Delete Media](actions/delete-media.md) | DELETE | Deletes an existing media item from Wistia. |
| [List Media](actions/list-media.md) | GET | Retrieves media from the Wistia account. |
| [Show Media](actions/show-media.md) | GET | Retrieves a media item from Wistia. |
| [Swap Media](actions/swap-media.md) | PUT | Swaps one Wistia media item with another. |
| [Translate Media](actions/translate-media.md) | POST | Translates the transcript for a Wistia media item. |
| [Update Media](actions/update-media.md) | PUT | Updates an existing media item in Wistia. |
| [Upload Or Import Media](actions/upload-or-import-media.md) | POST | Uploads a media file to Wistia or imports one by URL. |

### Media Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Media Aggregated Stats](actions/get-media-aggregated-stats.md) | GET | Retrieves aggregated stats for a Wistia media item. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Wistia](actions/search-wistia.md) | GET | Finds folders, media, and webinars in Wistia. |

