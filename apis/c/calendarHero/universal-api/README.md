# <img src="https://images.mindcloud.co/apps/icons/calendarhero-icon_1775660122479.png" alt="CalendarHero logo" width="28" height="28"> CalendarHero: Universal API

Schedule meetings, manage contacts, coordinate meeting requests, and administer CalendarHero account settings and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/calendarHero/latest
- **Category:** Productivity / Scheduling
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://calendarhero.com
- **Vendor API docs:** https://api.calendarhero.com/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Update Address](actions/update-address.md) | PUT | Updates an address in CalendarHero. |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Update Restricted Apps](actions/update-restricted-apps.md) | PUT | Updates restricted apps in CalendarHero. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in CalendarHero. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from CalendarHero. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from CalendarHero. |
| [Get Contact Count](actions/get-contact-count.md) | GET | Retrieves the contact count from CalendarHero. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in CalendarHero by search criteria. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in CalendarHero. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Directory](actions/create-directory.md) | POST | Creates a directory in CalendarHero. |
| [Delete Directory](actions/delete-directory.md) | DELETE | Deletes a directory from CalendarHero. |
| [Get Directory](actions/get-directory.md) | GET | Retrieves a directory from CalendarHero. |
| [List Directories](actions/list-directories.md) | GET | Retrieves directories from CalendarHero. |
| [Update Directory](actions/update-directory.md) | PUT | Updates a directory in CalendarHero. |

### Integrations

| Action | Method | Description |
| --- | --- | --- |
| [Get Providers](actions/get-providers.md) | GET | Retrieves providers from CalendarHero. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Update Work Location](actions/update-work-location.md) | PUT | Updates a work location in CalendarHero. |

### Meetings

| Action | Method | Description |
| --- | --- | --- |
| [Create Meeting Type](actions/create-meeting-type.md) | POST | Creates a meeting type in CalendarHero. |
| [Delete Meeting Type](actions/delete-meeting-type.md) | DELETE | Deletes a meeting type from CalendarHero. |
| [Get Meeting Categories](actions/get-meeting-categories.md) | GET | Retrieves meeting category stats from CalendarHero. |
| [Import Calendly Event Types](actions/import-calendly-event-types.md) | GET | Imports Calendly event types into CalendarHero. |
| [List Meeting Types](actions/list-meeting-types.md) | GET | Retrieves meeting types from CalendarHero. |
| [List Meetings](actions/list-meetings.md) | GET | Retrieves meetings from CalendarHero within a timeframe. |
| [Share Meeting Type](actions/share-meeting-type.md) | POST | Shares a meeting type in CalendarHero. |
| [Update Meeting Type](actions/update-meeting-type.md) | PUT | Updates a meeting type in CalendarHero. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Web Message](actions/create-web-message.md) | POST | Sends a web message to the CalendarHero assistant. |
| [Get Web Message](actions/get-web-message.md) | GET | Retrieves a web message reply from CalendarHero. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from CalendarHero. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Result](actions/get-search-result.md) | GET | Retrieves a search result from CalendarHero. |
| [Search Integrations](actions/search-integrations.md) | GET | Finds integrations in CalendarHero by query term. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Savings](actions/get-savings.md) | GET | Retrieves savings information from CalendarHero. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Meeting Task](actions/create-meeting-task.md) | POST | Creates a meeting task in CalendarHero. |
| [Delete Meeting Task](actions/delete-meeting-task.md) | DELETE | Deletes a meeting task from CalendarHero. |
| [List Meeting Tasks](actions/list-meeting-tasks.md) | GET | Retrieves meeting tasks from CalendarHero. |
| [Remind Meeting Task](actions/remind-meeting-task.md) | PUT | Sends a meeting task reminder in CalendarHero. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Update User Info](actions/update-user-info.md) | PUT | Updates user info in CalendarHero. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from CalendarHero. |
| [Update User](actions/update-user.md) | PUT | Updates a user in CalendarHero. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in CalendarHero. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from CalendarHero. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from CalendarHero. |

### Webhook Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Sample](actions/get-webhook-sample.md) | GET | Retrieves a webhook sample from CalendarHero. |

