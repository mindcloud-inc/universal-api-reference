# Zoho WorkDrive: Native API Reference

A consolidated summary of Zoho WorkDrive's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://workdrive.zoho.com/apidocs/v1
- **API base URL:** `{api_domain}/workdrive`

## Authentication

### OAuth 2.0

Connect Zoho WorkDrive with OAuth 2.0.

### Credentials

- **Base API URL:** `baseApiUrl` · required · The Zoho WorkDrive API base URL for your data center, such as https://www.zohoapis.com/workdrive/ or https://www.zohoapis.eu/workdrive/.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `WorkDrive.comments.CREATE,WorkDrive.files.CREATE,WorkDrive.files.READ,WorkDrive.labels.CREATE,WorkDrive.links.CREATE,WorkDrive.team.READ,WorkDrive.teamfolders.READ,WorkDrive.users.READ,ZohoSearch.securesearch.READ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.authorizeRequest.["accounts-server"]}}/oauth/v2/token.

[Official authentication documentation](https://workdrive.zoho.com/apidocs/v1/oauth2authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/vnd.api+json` |

Responses from this API use JSON.

## Pagination

Use `page[limit]` in the query string to set the page size (default 50; accepted range 1–1000). Use `page[offset]` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Label to File/Folder](actions/add-label-to-file-folder.md) | `POST /api/v1/labels/:labelId/relationships/files` | [docs](https://workdrive.zoho.com/apidocs/v1/labels/addlabeltofilefolder) |
| [Create Comment](actions/create-comment.md) | `POST /api/v1/comments` | [docs](https://workdrive.zoho.com/apidocs/v1/comments/createcomment) |
| [Create External Share Custom Link](actions/create-external-share-custom-link.md) | `POST /api/v1/links` | [docs](https://workdrive.zoho.com/apidocs/v1/externalsharing/createexternalsharecustomlink) |
| [Create Folder](actions/create-folder.md) | `POST /api/v1/files` | [docs](https://workdrive.zoho.com/apidocs/v1/folders/createfolder) |
| [Create Label](actions/create-label.md) | `POST /api/v1/labels` | [docs](https://workdrive.zoho.com/apidocs/v1/labels/createlabel) |
| [Get All Labels of the User](actions/get-all-labels-of-the-user.md) | `GET /api/v1/users/:teamMemberId/labels` | [docs](https://workdrive.zoho.com/apidocs/v1/labels/getalllabelsoftheuser) |
| [Get All Teams of User](actions/get-all-teams-of-user.md) | `GET /api/v1/users/:zuid/teams` | [docs](https://workdrive.zoho.com/apidocs/v1/users/getallteamsofuser) |
| [Get Current Team Member](actions/get-current-team-member.md) | `GET /api/v1/teams/:teamId/currentuser` | [docs](https://workdrive.zoho.com/apidocs/v1/teams/getcurrentteammember) |
| [Get File Comments](actions/get-file-comments.md) | `GET /api/v1/files/:resourceId/comments` | [docs](https://workdrive.zoho.com/apidocs/v1/filesfolders/getfilecomments) |
| [Get File/Folder Breadcrumbs](actions/get-file-folder-breadcrumbs.md) | `GET /api/v1/files/:resourceId/breadcrumbs` | [docs](https://workdrive.zoho.com/apidocs/v1/filesfolders/getfilefolderbreadcrumbs) |
| [Get File/Folder External Share Links](actions/get-file-folder-external-share-links.md) | `GET /api/v1/files/:resourceId/links` | [docs](https://workdrive.zoho.com/apidocs/v1/filesfolders/getfilefolderexternalsharelinks) |
| [Get File/Folder Info](actions/get-file-folder-info.md) | `GET /api/v1/files/:resourceId` | [docs](https://workdrive.zoho.com/apidocs/v1/filesfolders/getfilefolderinfo) |
| [Get Files in My Folders](actions/get-files-in-my-folders.md) | `GET /api/v1/privatespace/:myfolderId/files` | [docs](https://workdrive.zoho.com/apidocs/v1/myfoldersfiles/getfilesinmyfolders) |
| [Get Files in Shared with Me](actions/get-files-in-shared-with-me.md) | `GET /api/v1/users/:teamMemberId/incomingfiles` | [docs](https://workdrive.zoho.com/apidocs/v1/teammemberfiles/getfilesinsharedwithme) |
| [Get My Folders Id](actions/get-my-folders-id.md) | `GET /api/v1/users/:teamMemberId/privatespace` | [docs](https://workdrive.zoho.com/apidocs/v1/teammemberfiles/getmyfoldersid) |
| [Get Recent Files](actions/get-recent-files.md) | `GET /api/v1/users/:teamMemberId/recentfiles` | [docs](https://workdrive.zoho.com/apidocs/v1/teammemberfiles/getrecentfiles) |
| [Get Team Folder Files and Folders](actions/get-team-folder-files-and-folders.md) | `GET /api/v1/teamfolders/:teamfolderId/files` | [docs](https://workdrive.zoho.com/apidocs/v1/teamfolder/getteamfolderfilesandfolders) |
| [Get Team Folder Info](actions/get-team-folder-info.md) | `GET /api/v1/teamfolders/:teamfolderId` | [docs](https://workdrive.zoho.com/apidocs/v1/teamfolder/getteamfolderinfo) |
| [Get Team Folders in a Team](actions/get-team-folders-in-a-team.md) | `GET /api/v1/teams/:teamId/teamfolders` | [docs](https://workdrive.zoho.com/apidocs/v1/teams/getteamfoldersinateam) |
| [Get Team Info](actions/get-team-info.md) | `GET /api/v1/teams/:teamId` | [docs](https://workdrive.zoho.com/apidocs/v1/teams/getteaminfo) |
| [Get User Info](actions/get-user-info.md) | `GET /api/v1/users/me` | [docs](https://workdrive.zoho.com/apidocs/v1/users/getuserinfo) |
| [List Files/Folders inside a Folder](actions/list-files-folders-inside-a-folder.md) | `GET /api/v1/files/:folderId/files` | [docs](https://workdrive.zoho.com/apidocs/v1/folders/listfilesfoldersinsideafolder) |
| [Search across Team](actions/search-across-team.md) | `GET /api/v1/teams/:teamId/records` | [docs](https://workdrive.zoho.com/apidocs/v1/search/searchacrossteam) |
| [Search in My Folders](actions/search-in-my-folders.md) | `GET /api/v1/teams/:teamId/records` | [docs](https://workdrive.zoho.com/apidocs/v1/search/searchinmyfolders) |
