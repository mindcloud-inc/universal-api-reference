# Zoho WorkDrive Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zoho WorkDrive expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/get-files-in-my-folders?connectionId=$CONNECTION_ID&limit=25&offset=0&myfolderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zoho WorkDrive actions that support pagination

- [Get Files in My Folders](actions/get-files-in-my-folders.md)
- [Get Files in Shared with Me](actions/get-files-in-shared-with-me.md)
- [Get Recent Files](actions/get-recent-files.md)
- [Get Team Folder Files and Folders](actions/get-team-folder-files-and-folders.md)
- [Get Team Folders in a Team](actions/get-team-folders-in-a-team.md)
- [List Files/Folders inside a Folder](actions/list-files-folders-inside-a-folder.md)
- [Search across Team](actions/search-across-team.md)
- [Search in My Folders](actions/search-in-my-folders.md)
