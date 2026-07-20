# <img src="https://images.mindcloud.co/apps/icons/expiration-reminder_1782742781610.png" alt="Expiration Reminder logo" width="28" height="28"> Expiration Reminder: Universal API

Track expiration items, contacts, locations, and renewals

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/expirationReminder/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.expirationreminder.com
- **Vendor API docs:** https://developers.expirationreminder.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Log](actions/get-event-log.md) | GET | Retrieves an event log from Expiration Reminder. |
| [List Event Logs](actions/list-event-logs.md) | GET | Retrieves event logs from Expiration Reminder. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Type](actions/create-contact-type.md) | POST | Creates a new contact type in Expiration Reminder. |
| [Create Document Type](actions/create-document-type.md) | POST | Creates a new document type in Expiration Reminder. |
| [Delete Contact Type](actions/delete-contact-type.md) | DELETE | Deletes a contact type from Expiration Reminder. |
| [Delete Document Type](actions/delete-document-type.md) | DELETE | Deletes a document type from Expiration Reminder. |
| [Get Contact Type](actions/get-contact-type.md) | GET | Retrieves a contact type from Expiration Reminder. |
| [Get Document Type](actions/get-document-type.md) | GET | Retrieves a document type from Expiration Reminder. |
| [List Contact Types](actions/list-contact-types.md) | GET | Retrieves contact types from Expiration Reminder. |
| [List Document Types](actions/list-document-types.md) | GET | Retrieves document types from Expiration Reminder. |
| [Update Contact Type](actions/update-contact-type.md) | PUT | Updates an existing contact type in Expiration Reminder. |
| [Update Document Type](actions/update-document-type.md) | PUT | Updates an existing document type in Expiration Reminder. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Expiration Reminder. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Expiration Reminder. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Expiration Reminder. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Expiration Reminder. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Expiration Reminder. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Add File to Expiration Item](actions/add-file-to-expiration-item.md) | POST | Adds a file to an expiration item in Expiration Reminder. |
| [Get File Detail](actions/get-file-detail.md) | GET | Retrieves a file detail from Expiration Reminder. |
| [List Files Related to Expiration Items](actions/list-files-related-to-expiration-items.md) | GET | Retrieves files for expiration items from Expiration Reminder. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Expiration Item](actions/create-expiration-item.md) | POST | Creates a new expiration item in Expiration Reminder. |
| [Delete Expiration Item](actions/delete-expiration-item.md) | DELETE | Deletes an expiration item from Expiration Reminder. |
| [Get Expiration Item](actions/get-expiration-item.md) | GET | Retrieves an expiration item from Expiration Reminder. |
| [List Expiration Items](actions/list-expiration-items.md) | GET | Retrieves expiration items from Expiration Reminder. |
| [List Expiration Items for Contact](actions/list-expiration-items-for-contact.md) | GET | Retrieves expiration items for a contact from Expiration Reminder. |
| [Renew an expiration item](actions/renew-an-expiration-item-post.md) | PUT | Renews an expiration item in Expiration Reminder. |
| [Renew Expiration Item](actions/renew-expiration-item.md) | PUT | Renews an expiration item in Expiration Reminder. |
| [Update Contacts in Expiration Item](actions/update-contacts-in-expiration-item.md) | PUT | Updates contacts on an expiration item in Expiration Reminder. |
| [Update Expiration Item](actions/update-expiration-item.md) | PUT | Updates an existing expiration item in Expiration Reminder. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST | Creates a new location in Expiration Reminder. |
| [Delete Location](actions/delete-location.md) | DELETE | Deletes a location from Expiration Reminder. |
| [Get Location](actions/get-location.md) | GET | Retrieves a location from Expiration Reminder. |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from Expiration Reminder. |
| [Update Location](actions/update-location.md) | PUT | Updates an existing location in Expiration Reminder. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Expiration Reminder. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in Expiration Reminder. |
| [Delete Workspace](actions/delete-workspace.md) | DELETE | Deletes a workspace from Expiration Reminder. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Expiration Reminder. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Expiration Reminder. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates an existing workspace in Expiration Reminder. |

