# <img src="https://images.mindcloud.co/apps/icons/seafile-transparent-1024_1775150595535.png" alt="Seafile logo" width="28" height="28"> Seafile: Universal API

Store, sync, share, and manage files and libraries

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/seafile/latest
- **Category:** Content & Files / Storage
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.seafile.com/
- **Vendor API docs:** https://seafile-api.readme.io/reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get File Activities](actions/get-file-activities.md) | GET | Retrieves recent file activity events from Seafile. |

### Drives

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Library](actions/get-default-library.md) | GET | Retrieves the default library from Seafile. |
| [Get Library Info](actions/get-library-info.md) | GET | Retrieves details for a Seafile library. |
| [List Libraries](actions/list-libraries.md) | GET | Retrieves libraries from Seafile, optionally filtered by name. |
| [List Libraries Shared to Me](actions/list-libraries-shared-to-me.md) | GET | Retrieves Seafile libraries shared with the current user. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get File Detail](actions/get-file-detail.md) | GET | Retrieves details for a file in Seafile. |
| [Get File History](actions/get-file-history.md) | GET | Retrieves the version history for a file in Seafile. |
| [Search Files by Name in Library](actions/search-files-by-name-in-library.md) | GET | Finds files in a Seafile library by name. |
| [Search Files in Libraries](actions/search-files-in-libraries.md) | GET | Finds files across Seafile libraries by keyword. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Get Directory Detail](actions/get-directory-detail.md) | GET | Retrieves details for a directory in Seafile. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Info](actions/get-group-info.md) | GET | Retrieves details for a Seafile group. |
| [List Groups](actions/list-groups.md) | GET | Retrieves the groups available in Seafile. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Invitation](actions/get-invitation.md) | GET | Retrieves a Seafile invitation by token. |
| [Get Library Commit Info](actions/get-library-commit-info.md) | GET | Retrieves details for a Seafile library commit. |
| [Get Library History](actions/get-library-history.md) | GET | Retrieves the history of a Seafile library. |
| [Get Library Trash](actions/get-library-trash.md) | GET | Retrieves trash contents for a Seafile library. |
| [List All Share Links](actions/list-all-share-links.md) | GET | Retrieves all share links from Seafile. |
| [List Devices](actions/list-devices.md) | GET | Retrieves the current devices connected to Seafile. |
| [List Folder Download Items](actions/list-folder-download-items.md) | GET | Retrieves items from a Seafile folder download link. |
| [List Folder or File Share Links](actions/list-folder-or-file-share-links.md) | GET | Retrieves share links for a Seafile folder or file. |
| [List Invitations](actions/list-invitations.md) | GET | Retrieves the current invitations in Seafile. |
| [List Items in Directory](actions/list-items-in-directory.md) | GET | Retrieves items in a Seafile library directory. |
| [List Library Share Links](actions/list-library-share-links.md) | GET | Retrieves share links for a Seafile library. |
| [List Starred Items](actions/list-starred-items.md) | GET | Retrieves the starred items in Seafile. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves the current account information from Seafile. |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves the current user profile from Seafile. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Library Owner](actions/get-library-owner.md) | GET | Retrieves the owner of a Seafile library. |
| [List Group Members](actions/list-group-members.md) | GET | Retrieves members of a Seafile group. |
| [List Shared Library Users and Groups](actions/list-shared-library-users-and-groups.md) | GET | Retrieves users and groups a Seafile library is shared with. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Server Information](actions/get-server-information.md) | GET | Retrieves the current Seafile server information. |

