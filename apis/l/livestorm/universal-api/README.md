# <img src="https://images.mindcloud.co/apps/icons/images-2_1773401395269.png" alt="Livestorm logo" width="28" height="28"> Livestorm: Universal API

Livestorm: manage webinars, virtual events, sessions, registrants, people, hosts, and webhooks from the Livestorm Public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/livestorm/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://livestorm.co
- **Vendor API docs:** https://developers.livestorm.co/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Authentication](actions/test-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Test Authentication](actions/test-authentication.md) | GET | Tests authentication with the Livestorm API. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Livestorm. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from Livestorm. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Livestorm. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Livestorm. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Livestorm. |

### Event Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Person](actions/get-event-person.md) | GET | Retrieves an event person from Livestorm. |
| [List Event People](actions/list-event-people.md) | GET | Retrieves people for an event from Livestorm. |

### Event Tag

| Action | Method | Description |
| --- | --- | --- |
| [Assign Event Tag](actions/assign-event-tag.md) | POST | Assigns a tag to an event in Livestorm. |
| [Remove Event Tag](actions/remove-event-tag.md) | DELETE | Removes a tag from an event in Livestorm. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from Livestorm. |

### People Attribute

| Action | Method | Description |
| --- | --- | --- |
| [List People Attributes](actions/list-people-attributes.md) | GET | Retrieves people attributes from Livestorm. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from Livestorm. |
| [List People](actions/list-people.md) | GET | Retrieves people from Livestorm. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Session](actions/create-event-session.md) | POST | Creates a new session for an event in Livestorm. |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes an existing session from Livestorm. |
| [Get Session](actions/get-session.md) | GET | Retrieves a session from Livestorm. |
| [List Event Sessions](actions/list-event-sessions.md) | GET | Retrieves sessions for an event from Livestorm. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves sessions from Livestorm. |
| [Update Session](actions/update-session.md) | PUT | Updates an existing session in Livestorm. |

### Session Person

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Register Session People](actions/bulk-register-session-people.md) | POST | Registers multiple people for a session in Livestorm. |
| [Delete Session Person](actions/delete-session-person.md) | DELETE | Removes a person from a session in Livestorm. |
| [Get Session Person](actions/get-session-person.md) | GET | Retrieves a session person from Livestorm. |
| [List Session People](actions/list-session-people.md) | GET | Retrieves people for a session from Livestorm. |
| [Register Session Person](actions/register-session-person.md) | POST | Registers a person for a session in Livestorm. |

### Session Question

| Action | Method | Description |
| --- | --- | --- |
| [List Session Questions](actions/list-session-questions.md) | GET | Retrieves questions for a session from Livestorm. |

### Session Recording

| Action | Method | Description |
| --- | --- | --- |
| [List Session Recordings](actions/list-session-recordings.md) | GET | Retrieves recordings for a session from Livestorm. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Livestorm. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Livestorm. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Livestorm. |

