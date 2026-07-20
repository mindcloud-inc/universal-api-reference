# Zoho WorkDrive Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Zoho WorkDrive expects, and each action page lists the fields available to sort.

## Zoho WorkDrive actions that support sorting

- [Get Files in My Folders](actions/get-files-in-my-folders.md)
- [Get Files in Shared with Me](actions/get-files-in-shared-with-me.md)
- [Get Team Folder Files and Folders](actions/get-team-folder-files-and-folders.md)
- [List Files/Folders inside a Folder](actions/list-files-folders-inside-a-folder.md)
- [Search across Team](actions/search-across-team.md)
- [Search in My Folders](actions/search-in-my-folders.md)
