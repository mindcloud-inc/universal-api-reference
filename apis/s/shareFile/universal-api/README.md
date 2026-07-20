# <img src="https://images.mindcloud.co/apps/icons/share-file-mobile_1773755719844.png" alt="ShareFile logo" width="28" height="28"> ShareFile: Universal API

ShareFile integration for managing files, folders, shares, users, groups, accounts, zones, and sessions via the ShareFile API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shareFile/latest
- **Category:** Content & Files / Storage
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sharefile.com/
- **Vendor API docs:** https://api.sharefile.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Session](actions/get-session.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/get-session?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |
| [Get Current Account](actions/get-current-account.md) | GET |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST |  |
| [Delete Group](actions/delete-group.md) | DELETE |  |
| [Get Group](actions/get-group.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |
| [Update Group](actions/update-group.md) | PUT |  |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Delete Item](actions/delete-item.md) | DELETE |  |
| [Get Home Folder for Current User](actions/get-home-folder-for-current-user.md) | GET |  |
| [Get Item](actions/get-item.md) | GET |  |
| [List Item Children](actions/list-item-children.md) | GET |  |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Get Session](actions/get-session.md) | GET |  |

### Share

| Action | Method | Description |
| --- | --- | --- |
| [Delete Share](actions/delete-share.md) | DELETE |  |
| [Get Share](actions/get-share.md) | GET |  |
| [List Shares](actions/list-shares.md) | GET |  |
| [Send Share](actions/send-share.md) | POST |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create Client User](actions/create-client-user.md) | POST |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |
| [Update User](actions/update-user.md) | PUT |  |

### Zone

| Action | Method | Description |
| --- | --- | --- |
| [Get Zone](actions/get-zone.md) | GET |  |
| [List Zones](actions/list-zones.md) | GET |  |

