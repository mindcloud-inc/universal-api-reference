# <img src="https://images.mindcloud.co/apps/icons/brand-logos-1757669599391-20221022-crush-logo_1774465011322.png" alt="CRUSH logo" width="28" height="28"> CRUSH: Universal API

Capture, organize, and analyze voice notes with CRUSH AI

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cRUSH/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://crushthememory.com
- **Vendor API docs:** https://app.crushthememory.com/dashboard

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List API Tokens](actions/list-api-tokens.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/list-api-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Api Token

| Action | Method | Description |
| --- | --- | --- |
| [List API Tokens](actions/list-api-tokens.md) | GET |  |

### Audio Url

| Action | Method | Description |
| --- | --- | --- |
| [Get Audio Download URL](actions/get-audio-download-url.md) | GET |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET |  |

### Folder Metadata

| Action | Method | Description |
| --- | --- | --- |
| [List Folder Metadata](actions/list-folder-metadata.md) | GET |  |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Get Note](actions/get-note.md) | GET |  |
| [List Notes](actions/list-notes.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET |  |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET |  |

