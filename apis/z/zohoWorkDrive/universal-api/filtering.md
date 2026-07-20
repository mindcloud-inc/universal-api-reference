# Zoho WorkDrive Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Zoho WorkDrive expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Zoho WorkDrive actions that support filtering

- [Get File/Folder External Share Links](actions/get-file-folder-external-share-links.md)
- [Get Files in My Folders](actions/get-files-in-my-folders.md)
- [Get Files in Shared with Me](actions/get-files-in-shared-with-me.md)
- [Get Recent Files](actions/get-recent-files.md)
- [Get Team Folder Files and Folders](actions/get-team-folder-files-and-folders.md)
- [Get Team Folders in a Team](actions/get-team-folders-in-a-team.md)
- [List Files/Folders inside a Folder](actions/list-files-folders-inside-a-folder.md)
- [Search across Team](actions/search-across-team.md)
- [Search in My Folders](actions/search-in-my-folders.md)
