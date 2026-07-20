# <img src="https://images.mindcloud.co/apps/icons/microsoft-logo-256px_1773865938073.png" alt="Microsoft 365 logo" width="28" height="28"> Microsoft 365: Universal API

Access Microsoft 365 and Microsoft Graph data, including the signed-in user's profile and other Microsoft 365 resources, through delegated OAuth 2.0 connections.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoft365/latest
- **Actions:** 57
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.microsoft.com/microsoft-365
- **Vendor API docs:** https://learn.microsoft.com/en-us/graph/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (57)

### Calendars

| Action | Method | Description |
| --- | --- | --- |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves calendars from Microsoft 365. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Microsoft 365. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Microsoft 365. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Microsoft 365. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Microsoft 365. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in Microsoft 365. |

### Drive Items

| Action | Method | Description |
| --- | --- | --- |
| [List My Drive Items](actions/list-my-drive-items.md) | GET | Retrieves items in your drive from Microsoft 365. |

### Drives

| Action | Method | Description |
| --- | --- | --- |
| [Get My Drive](actions/get-my-drive.md) | GET | Retrieves your drive from Microsoft 365. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Accept Event](actions/accept-event.md) | PUT | Accepts an event in Microsoft 365. |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Microsoft 365. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an event from Microsoft 365. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Microsoft 365. |
| [List Calendar View](actions/list-calendar-view.md) | GET | Retrieves calendar view events from Microsoft 365. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Microsoft 365. |
| [Update Event](actions/update-event.md) | PUT | Updates an event in Microsoft 365. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Downloads a file from Microsoft 365. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Microsoft 365. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a folder in a Microsoft 365 drive. |
| [List Child Mail Folders](actions/list-child-mail-folders.md) | GET | Retrieves child mail folders from Microsoft 365. |
| [List Folder Items](actions/list-folder-items.md) | GET | Retrieves items in a folder from Microsoft 365. |
| [List Mail Folders](actions/list-mail-folders.md) | GET | Retrieves mail folders from Microsoft 365. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Entra Group Users](actions/list-entra-group-users.md) | GET | Retrieves Entra group members from Microsoft 365. |
| [List Entra Groups](actions/list-entra-groups.md) | GET | Retrieves Entra groups from Microsoft 365. |

### Message Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Get Message Attachment](actions/get-message-attachment.md) | GET | Retrieves a message attachment from Microsoft 365. |
| [List Message Attachments](actions/list-message-attachments.md) | GET | Retrieves message attachments from Microsoft 365. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Message](actions/create-draft-message.md) | POST | Creates a draft message in Microsoft 365. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes a message from Microsoft 365. |
| [Forward Message](actions/forward-message.md) | POST | Forwards a message from Microsoft 365. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Microsoft 365. |
| [List Inbox Messages](actions/list-inbox-messages.md) | GET | Retrieves inbox messages from Microsoft 365. |
| [List Messages in Folder](actions/list-messages-in-folder.md) | GET | Retrieves messages in a mail folder from Microsoft 365. |
| [Move Message](actions/move-message.md) | PUT | Moves a message to another folder in Microsoft 365. |
| [Reply All to Message](actions/reply-all-to-message.md) | POST | Replies to all recipients on a message in Microsoft 365. |
| [Reply to Message](actions/reply-to-message.md) | POST | Replies to a message in Microsoft 365. |
| [Send Draft Message](actions/send-draft-message.md) | PUT | Sends a draft message from Microsoft 365. |
| [Send Mail](actions/send-mail.md) | POST | Sends an email from Microsoft 365. |
| [Update Draft Message](actions/update-draft-message.md) | PUT | Updates a draft message in Microsoft 365. |

### Notebooks

| Action | Method | Description |
| --- | --- | --- |
| [Create Notebook](actions/create-notebook.md) | POST | Creates a new notebook in Microsoft 365. |
| [List Notebooks](actions/list-notebooks.md) | GET | Retrieves notebooks from Microsoft 365. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Page](actions/get-page.md) | GET | Retrieves a OneNote page from Microsoft 365. |
| [List Pages](actions/list-pages.md) | GET | Retrieves OneNote pages from Microsoft 365. |

### Range

| Action | Method | Description |
| --- | --- | --- |
| [Update Range Values](actions/update-range-values.md) | PUT | Updates worksheet range values in Microsoft 365. |

### Sections

| Action | Method | Description |
| --- | --- | --- |
| [Create Section](actions/create-section.md) | POST | Creates a new section in Microsoft 365. |
| [List Sections](actions/list-sections.md) | GET | Retrieves OneNote sections from Microsoft 365. |

### Task Lists

| Action | Method | Description |
| --- | --- | --- |
| [List Task Lists](actions/list-task-lists.md) | GET | Retrieves task lists from Microsoft 365. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Microsoft 365. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes a task from Microsoft 365. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Microsoft 365. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from a Microsoft 365 task list. |
| [Update Task](actions/update-task.md) | PUT | Updates a task in Microsoft 365. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET | Retrieves your Microsoft 365 profile. |
| [List Entra User Changes](actions/list-entra-user-changes.md) | GET | Retrieves Entra user changes from Microsoft 365. |
| [List Entra Users](actions/list-entra-users.md) | GET | Retrieves Entra users from Microsoft 365. |

### Workbook

| Action | Method | Description |
| --- | --- | --- |
| [Create Workbook](actions/create-workbook.md) | POST | Creates a workbook in Microsoft 365. |

### Workbook Range

| Action | Method | Description |
| --- | --- | --- |
| [Get Worksheet Used Range](actions/get-worksheet-used-range.md) | GET | Retrieves a worksheet's used range from Microsoft 365. |

### Worksheet

| Action | Method | Description |
| --- | --- | --- |
| [Create Worksheet in Workbook](actions/create-worksheet-in-workbook.md) | POST | Creates a worksheet in a Microsoft 365 workbook. |
| [List Worksheets](actions/list-worksheets.md) | GET | Retrieves worksheets from a Microsoft 365 workbook. |

