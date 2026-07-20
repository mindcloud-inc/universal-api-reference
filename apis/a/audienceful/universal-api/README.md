# <img src="https://images.mindcloud.co/apps/icons/audienceful_1774359338423.png" alt="Audienceful logo" width="28" height="28"> Audienceful: Universal API

Manage people, custom fields, events, and send reports.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/audienceful/latest
- **Category:** Marketing
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.audienceful.com
- **Vendor API docs:** https://developer.audienceful.com/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List People](actions/list-people.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/list-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a new person in Audienceful. |
| [Delete Person](actions/delete-person.md) | DELETE | Deletes an existing person from Audienceful. |
| [List People](actions/list-people.md) | GET | Retrieves a list of people from Audienceful. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in Audienceful. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Event](actions/trigger-event.md) | POST | Triggers Audienceful automations by event name. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a new custom field in Audienceful. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes an existing custom field from Audienceful. |
| [List Fields](actions/list-fields.md) | GET | Retrieves a list of custom fields from Audienceful. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List Send Reports](actions/list-send-reports.md) | GET | Retrieves a list of send reports from Audienceful. |

