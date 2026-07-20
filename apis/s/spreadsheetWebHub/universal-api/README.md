# <img src="https://images.mindcloud.co/apps/icons/spreadsheet-web-hub_1774382626076.png" alt="SpreadsheetWeb Hub logo" width="28" height="28"> SpreadsheetWeb Hub: Universal API

Run calculations and manage SpreadsheetWeb Hub applications, users, and tags

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/spreadsheetWebHub/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.spreadsheetweb.com
- **Vendor API docs:** https://api.spreadsheetweb.com/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Calculate Multiple](actions/calculate-multiple.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/calculate-multiple?connectionId=$CONNECTION_ID&request.applicationId=string&request.workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Application](actions/get-application.md) | GET | Retrieves an application from SpreadsheetWeb Hub. |
| [Get Application by Slug](actions/get-application-by-slug.md) | GET | Retrieves an application from SpreadsheetWeb Hub by slug. |
| [List Application Tag Relationships](actions/list-application-tag-relationships.md) | GET | Retrieves application tag relationships from SpreadsheetWeb Hub. |
| [List Applications](actions/list-applications.md) | GET | Retrieves applications from a SpreadsheetWeb Hub workspace. |
| [List Applications by IDs](actions/list-applications-by-ids.md) | GET | Retrieves multiple applications from SpreadsheetWeb Hub by ID. |

### Calculation

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Multiple](actions/calculate-multiple.md) | GET | Performs multiple calculations in SpreadsheetWeb Hub. |
| [Calculate Multiple Async](actions/calculate-multiple-async.md) | GET | Performs multiple asynchronous calculations in SpreadsheetWeb Hub. |
| [Calculate Single](actions/calculate-single.md) | GET | Performs a single calculation in SpreadsheetWeb Hub. |
| [Calculate Single Simple](actions/calculate-single-simple.md) | GET | Performs a simplified single calculation in SpreadsheetWeb Hub. |
| [Get Calculation Progress](actions/get-calculation-progress.md) | GET | Retrieves calculation progress from SpreadsheetWeb Hub. |
| [Prepopulate Instance](actions/prepopulate-instance.md) | GET | Prepopulates an application instance in SpreadsheetWeb Hub. |

### Data Share

| Action | Method | Description |
| --- | --- | --- |
| [Create Data Share Link](actions/create-data-share-link.md) | POST | Creates a new data share link in SpreadsheetWeb Hub. |
| [Delete Data Share Link](actions/delete-data-share-link.md) | DELETE | Deletes an existing data share link from SpreadsheetWeb Hub. |
| [List Data Share Links](actions/list-data-share-links.md) | GET | Retrieves data share links from SpreadsheetWeb Hub. |
| [Update Data Share Link](actions/update-data-share-link.md) | PUT | Updates an existing data share link in SpreadsheetWeb Hub. |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace Invite](actions/create-workspace-invite.md) | POST | Creates a new workspace invite in SpreadsheetWeb Hub. |
| [List Workspace Invites](actions/list-workspace-invites.md) | GET | Retrieves workspace invites from SpreadsheetWeb Hub. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in SpreadsheetWeb Hub. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from SpreadsheetWeb Hub. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from SpreadsheetWeb Hub. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from a SpreadsheetWeb Hub workspace. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in SpreadsheetWeb Hub. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from SpreadsheetWeb Hub. |
| [List Users](actions/list-users.md) | GET | Retrieves users from a SpreadsheetWeb Hub workspace. |

