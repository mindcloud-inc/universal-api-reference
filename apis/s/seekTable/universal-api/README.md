# <img src="https://images.mindcloud.co/apps/icons/seek-table_1775153975969.png" alt="SeekTable logo" width="28" height="28"> SeekTable: Universal API

Generate, export, and share SeekTable reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/seekTable/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.seektable.com/
- **Vendor API docs:** https://www.seektable.com/help/web-api-integration

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Reports](actions/list-reports.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/list-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Account Backup

| Action | Method | Description |
| --- | --- | --- |
| [Backup Account Data](actions/backup-account-data.md) | GET | Retrieves a backup export from SeekTable. |

### Cube

| Action | Method | Description |
| --- | --- | --- |
| [Get Cube Info](actions/get-cube-info.md) | GET | Retrieves a SeekTable cube by cube ID. |
| [List Cubes](actions/list-cubes.md) | GET | Retrieves cubes from your SeekTable account. |
| [Upload CSV File](actions/upload-csv-file.md) | POST | Uploads a CSV file to a SeekTable cube. |

### Dashboards

| Action | Method | Description |
| --- | --- | --- |
| [Export Dashboard](actions/export-dashboard.md) | GET | Exports a SeekTable dashboard in the requested format. |
| [List Dashboards](actions/list-dashboards.md) | GET | Retrieves dashboards from your SeekTable account. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Add Users To Team Group](actions/add-users-to-team-group.md) | POST | Adds users to a SeekTable team group. |
| [Create Team Group](actions/create-team-group.md) | POST | Creates a new team group in SeekTable. |
| [Delete Team Group](actions/delete-team-group.md) | DELETE | Deletes an existing team group from SeekTable. |
| [List Team Group Members](actions/list-team-group-members.md) | GET | Retrieves members from a SeekTable team group. |
| [List Team Groups](actions/list-team-groups.md) | GET | Retrieves team groups from a SeekTable account. |
| [Remove Users From Team Group](actions/remove-users-from-team-group.md) | DELETE | Removes users from a SeekTable team group. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Report Info](actions/get-report-info.md) | GET | Retrieves a SeekTable report by report ID. |
| [List Reports](actions/list-reports.md) | GET | Retrieves saved reports from your SeekTable account. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Export Report](actions/export-report.md) | GET | Exports a SeekTable report in the requested format. |
| [Share Report By Email](actions/share-report-by-email.md) | POST | Shares a SeekTable report by email. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add Team Members](actions/add-team-members.md) | POST | Adds team members to a SeekTable account. |
| [Assign Groups For Team Members](actions/assign-groups-for-team-members.md) | PUT | Assigns team groups to SeekTable team members. |
| [Create User Account](actions/create-user-account.md) | POST | Creates a new user account in SeekTable. |
| [Delete User Account](actions/delete-user-account.md) | DELETE | Deletes an existing user account from SeekTable. |
| [Get User Account](actions/get-user-account.md) | GET | Retrieves a SeekTable user account by ID. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from a SeekTable account. |
| [List User Accounts](actions/list-user-accounts.md) | GET | Retrieves user accounts from a SeekTable installation. |
| [Remove Team Members](actions/remove-team-members.md) | DELETE | Removes team members from a SeekTable account. |
| [Update User Account](actions/update-user-account.md) | PUT | Updates an existing user account in SeekTable. |

