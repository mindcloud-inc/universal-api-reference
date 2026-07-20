# <img src="https://images.mindcloud.co/apps/icons/hack-md_1774985286316.png" alt="HackMD logo" width="28" height="28"> HackMD: Universal API

HackMD is a collaborative markdown note-taking and documentation platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hackMD/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hackmd.io
- **Vendor API docs:** https://api.hackmd.io/v1/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST |  |
| [Delete Note](actions/delete-note.md) | DELETE |  |
| [Get Note](actions/get-note.md) | GET |  |
| [List Note History](actions/list-note-history.md) | GET |  |
| [List Notes](actions/list-notes.md) | GET |  |
| [Update Note](actions/update-note.md) | PUT |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

