# <img src="https://images.mindcloud.co/apps/icons/pastefy_1777038938991.png" alt="Pastefy logo" width="28" height="28"> Pastefy: Universal API

Share, organize, and manage pastes, folders, and code snippets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pastefy/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pastefy.app
- **Vendor API docs:** https://docs.pastefy.app/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pastefy/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST |  |
| [Delete API Key](actions/delete-api-key.md) | DELETE |  |
| [List API Keys](actions/list-api-keys.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Paste](actions/create-paste.md) | POST |  |
| [Delete Paste](actions/delete-paste.md) | DELETE |  |
| [Get Paste](actions/get-paste.md) | GET |  |
| [Get Paste Raw Content](actions/get-paste-raw-content.md) | GET |  |
| [List Pastes](actions/list-pastes.md) | GET |  |
| [List Starred Pastes](actions/list-starred-pastes.md) | GET |  |
| [List Trending Public Pastes](actions/list-trending-public-pastes.md) | GET |  |
| [List User Pastes](actions/list-user-pastes.md) | GET |  |
| [Star Paste](actions/star-paste.md) | PUT |  |
| [Unstar Paste](actions/unstar-paste.md) | PUT |  |
| [Update Paste](actions/update-paste.md) | PUT |  |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |
| [List Folders](actions/list-folders.md) | GET |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get User Overview](actions/get-user-overview.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

