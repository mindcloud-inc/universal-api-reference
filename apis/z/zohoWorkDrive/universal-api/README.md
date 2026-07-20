# <img src="https://images.mindcloud.co/apps/icons/zoho-workdrive_1775233260584.png" alt="Zoho WorkDrive logo" width="28" height="28"> Zoho WorkDrive: Universal API

Browse files, search folders, and manage team folders

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoWorkDrive/latest
- **Category:** Content & Files / Storage
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/workdrive/
- **Vendor API docs:** https://workdrive.zoho.com/apidocs/v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Breadcrumb

| Action | Method | Description |
| --- | --- | --- |
| [Get File/Folder Breadcrumbs](actions/get-file-folder-breadcrumbs.md) | GET | Retrieves file or folder breadcrumbs from Zoho WorkDrive. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Zoho WorkDrive. |
| [Get File Comments](actions/get-file-comments.md) | GET | Retrieves comments for a Zoho WorkDrive file. |

### External Share

| Action | Method | Description |
| --- | --- | --- |
| [Create External Share Custom Link](actions/create-external-share-custom-link.md) | POST | Creates an external share link in Zoho WorkDrive. |
| [Get File/Folder External Share Links](actions/get-file-folder-external-share-links.md) | GET | Retrieves external share links for a Zoho WorkDrive file or folder. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get Files in My Folders](actions/get-files-in-my-folders.md) | GET | Retrieves files and folders from My Folders in Zoho WorkDrive. |

### File Or Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get File/Folder Info](actions/get-file-folder-info.md) | GET | Retrieves file or folder details from Zoho WorkDrive. |
| [Get Team Folder Files and Folders](actions/get-team-folder-files-and-folders.md) | GET | Retrieves files and folders from a Zoho WorkDrive team folder. |
| [List Files/Folders inside a Folder](actions/list-files-folders-inside-a-folder.md) | GET | Retrieves files and folders from a Zoho WorkDrive folder. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Zoho WorkDrive. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [Add Label to File/Folder](actions/add-label-to-file-folder.md) | POST | Adds a label to a Zoho WorkDrive file or folder. |
| [Create Label](actions/create-label.md) | POST | Creates a new label in Zoho WorkDrive. |
| [Get All Labels of the User](actions/get-all-labels-of-the-user.md) | GET | Retrieves labels for a Zoho WorkDrive user. |

### My Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get My Folders Id](actions/get-my-folders-id.md) | GET | Retrieves private-space folder details from Zoho WorkDrive. |

### Recent File

| Action | Method | Description |
| --- | --- | --- |
| [Get Recent Files](actions/get-recent-files.md) | GET | Retrieves recent files from Zoho WorkDrive. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search across Team](actions/search-across-team.md) | GET | Finds files and folders in Zoho WorkDrive across a team. |
| [Search in My Folders](actions/search-in-my-folders.md) | GET | Finds files and folders in Zoho WorkDrive within My Folders. |

### Shared File

| Action | Method | Description |
| --- | --- | --- |
| [Get Files in Shared with Me](actions/get-files-in-shared-with-me.md) | GET | Retrieves files shared with a Zoho WorkDrive user. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get All Teams of User](actions/get-all-teams-of-user.md) | GET | Retrieves teams for a Zoho WorkDrive user. |
| [Get Team Info](actions/get-team-info.md) | GET | Retrieves team details from Zoho WorkDrive. |

### Team Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Folder Info](actions/get-team-folder-info.md) | GET | Retrieves team folder details from Zoho WorkDrive. |
| [Get Team Folders in a Team](actions/get-team-folders-in-a-team.md) | GET | Retrieves team folders from a Zoho WorkDrive team. |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Team Member](actions/get-current-team-member.md) | GET | Retrieves the current team member from Zoho WorkDrive. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves current user details from Zoho WorkDrive. |

