# <img src="https://images.mindcloud.co/apps/icons/images-4_1774625858641.png" alt="Asset Panda logo" width="28" height="28"> Asset Panda: Universal API

Track assets, manage inventory, and organize records and reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/assetPanda/latest
- **Category:** Support / Field Service
- **Actions:** 50
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.assetpanda.com
- **Vendor API docs:** https://team-asset-panda.readme.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Self Details](actions/retrieve-self-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/retrieve-self-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (50)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account User](actions/create-account-user.md) | POST | Creates a new user account in Asset Panda. |
| [Delete Account](actions/delete-account.md) | DELETE | Deletes an account from Asset Panda. |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves account details from Asset Panda. |

### Action

| Action | Method | Description |
| --- | --- | --- |
| [Get Action](actions/get-action.md) | GET | Retrieves an action from Asset Panda. |
| [List Actions](actions/list-actions.md) | GET | Retrieves actions from Asset Panda. |

### Action Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Multiple Action Fields](actions/create-multiple-action-fields.md) | POST | Creates multiple action fields in Asset Panda. |
| [Delete Action Field](actions/delete-action-field.md) | DELETE | Deletes an action field from Asset Panda. |
| [List Action Fields](actions/list-action-fields.md) | GET | Retrieves action fields from Asset Panda. |
| [Update Action Field](actions/update-action-field.md) | PUT | Updates an action field in Asset Panda. |

### Action Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Action Group](actions/get-action-group.md) | GET | Retrieves an action group from Asset Panda. |

### Action Object

| Action | Method | Description |
| --- | --- | --- |
| [Create Multiple](actions/create-multiple.md) | POST | Creates multiple action objects in Asset Panda. |
| [List Action Objects](actions/list-action-objects.md) | GET | Retrieves action objects from Asset Panda. |
| [List Returnable Action Objects](actions/list-returnable-action-objects.md) | GET | Retrieves returnable action objects from Asset Panda. |
| [Return Multiple](actions/return-multiple.md) | GET | Returns multiple objects in Asset Panda. |
| [Return Object](actions/return-object.md) | GET | Returns an object in Asset Panda. |

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Attachment](actions/delete-attachment.md) | DELETE | Deletes an attachment from Asset Panda. |
| [Link Attachment to Object](actions/link-attachment-to-object.md) | PUT | Links an attachment to an object in Asset Panda. |
| [List Attachments](actions/list-attachments.md) | GET | Retrieves attachments from Asset Panda. |
| [Update Attachment](actions/update-attachment.md) | PUT | Updates an attachment in Asset Panda. |

### Attachment Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new attachment folder in Asset Panda. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes an attachment folder from Asset Panda. |

### Change Log

| Action | Method | Description |
| --- | --- | --- |
| [List Change Logs](actions/list-change-logs.md) | GET | Retrieves change logs from Asset Panda. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Asset Panda. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Asset Panda. |

### Group Action

| Action | Method | Description |
| --- | --- | --- |
| [Create Group Action](actions/create-group-action.md) | POST | Creates a new group action in Asset Panda. |
| [List Group Actions](actions/list-group-actions.md) | GET | Retrieves group actions from Asset Panda. |

### Group Field

| Action | Method | Description |
| --- | --- | --- |
| [List Group Action Fields](actions/list-group-action-fields.md) | GET | Retrieves group action fields from Asset Panda. |
| [List Group Fields](actions/list-group-fields.md) | GET | Retrieves group fields from Asset Panda. |

### Group Object

| Action | Method | Description |
| --- | --- | --- |
| [Archive Objects](actions/archive-objects.md) | PUT | Archives objects in Asset Panda. |
| [Attach Attachment to Object](actions/attach-attachment-to-object.md) | PUT | Attaches an attachment to an object in Asset Panda. |
| [Create Object](actions/create-object.md) | POST | Creates one or more objects in Asset Panda. |
| [Detach Attachment from Object](actions/detach-attachment-from-object.md) | PUT | Detaches an attachment from an object in Asset Panda. |
| [Search Objects](actions/search-objects.md) | GET | Finds objects in Asset Panda. |
| [Unarchive Objects](actions/unarchive-objects.md) | PUT | Unarchives objects in Asset Panda. |
| [Update Group Object](actions/update-group-object.md) | PUT | Updates a group object in Asset Panda. |
| [Update Multiple Objects](actions/update-multiple-objects.md) | PUT | Updates multiple objects in Asset Panda. |

### Group Status

| Action | Method | Description |
| --- | --- | --- |
| [List Group Statuses](actions/list-group-statuses.md) | GET | Retrieves group statuses from Asset Panda. |

### Linked Field

| Action | Method | Description |
| --- | --- | --- |
| [List Linked Fields](actions/list-linked-fields.md) | GET | Retrieves linked fields from Asset Panda. |

### Linked Object

| Action | Method | Description |
| --- | --- | --- |
| [List Linked Objects](actions/list-linked-objects.md) | GET | Retrieves linked objects from Asset Panda. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Create Report](actions/create-report.md) | POST | Creates a new report in Asset Panda. |
| [Delete Report](actions/delete-report.md) | DELETE | Deletes a report from Asset Panda. |
| [Generate Report](actions/generate-report.md) | GET | Generates a report in Asset Panda. |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from Asset Panda. |
| [Update Report](actions/update-report.md) | PUT | Updates a report in Asset Panda. |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Settings](actions/retrieve-settings.md) | GET | Retrieves settings from Asset Panda. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List User Templates](actions/list-user-templates.md) | GET | Retrieves user templates from Asset Panda. |
| [Retrieve Self Details](actions/retrieve-self-details.md) | GET | Retrieves your user details from Asset Panda. |
| [Update User](actions/update-user.md) | PUT | Updates a user in Asset Panda. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Asset Panda. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Asset Panda. |

