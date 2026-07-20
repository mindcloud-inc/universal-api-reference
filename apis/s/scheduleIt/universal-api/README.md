# <img src="https://images.mindcloud.co/apps/icons/schedule-it_1774385899152.png" alt="Schedule It logo" width="28" height="28"> Schedule It: Universal API

Schedule resources, staff, rooms, and equipment

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scheduleIt/latest
- **Category:** Productivity / Scheduling
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.scheduleit.com
- **Vendor API docs:** https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Groups](actions/list-groups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Schedule It. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from Schedule It. |
| [Get Event](actions/get-event.md) | GET | Retrieves event details from Schedule It. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Schedule It. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Schedule It. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Schedule It. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Schedule It. |
| [Get Group](actions/get-group.md) | GET | Retrieves group details from Schedule It. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Schedule It. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Schedule It. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [Get Label](actions/get-label.md) | GET | Retrieves label details from Schedule It. |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels from Schedule It. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Create Resource](actions/create-resource.md) | POST | Creates a new resource in Schedule It. |
| [Delete Resource](actions/delete-resource.md) | DELETE | Deletes an existing resource from Schedule It. |
| [Get Resource](actions/get-resource.md) | GET | Retrieves resource details from Schedule It. |
| [List Resources](actions/list-resources.md) | GET | Retrieves resources from Schedule It. |
| [Update Resource](actions/update-resource.md) | PUT | Updates an existing resource in Schedule It. |

