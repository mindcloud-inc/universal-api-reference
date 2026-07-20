# <img src="https://images.mindcloud.co/apps/icons/95335b0-small-logo-x-favicon1b_1775140122622.png" alt="Pipeless Recommendations logo" width="28" height="28"> Pipeless Recommendations: Universal API

Read and write Pipeless recommendation data, activity feeds, events, objects, and relationship statistics through the official Pipeless API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pipelessRecommendations/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pipeless.io
- **Vendor API docs:** https://docs.pipeless.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Recent Events](actions/get-recent-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-recent-events?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity Actions Feed](actions/get-activity-actions-feed.md) | GET | Retrieves grouped activity actions for an object in Pipeless Recommendations. |
| [Get Activity Feed](actions/get-activity-feed.md) | GET | Retrieves an activity feed for an object in Pipeless Recommendations. |
| [Get Activity On Object](actions/get-activity-on-object.md) | GET | Retrieves activity on a target object in Pipeless Recommendations. |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Delete All Objects By Type](actions/delete-all-objects-by-type.md) | DELETE | Deletes all objects of one type from Pipeless Recommendations. |
| [Delete Object](actions/delete-object.md) | DELETE | Deletes an object and its related data from Pipeless Recommendations. |
| [Edit Object](actions/edit-object.md) | PUT | Updates an existing object in Pipeless Recommendations. |
| [Get Object](actions/get-object.md) | GET | Retrieves a single object from Pipeless Recommendations. |
| [Get Recommended Content](actions/get-recommended-content.md) | GET | Retrieves recommended content in Pipeless Recommendations. |
| [Get Related Content](actions/get-related-content.md) | GET | Retrieves related content in Pipeless Recommendations. |
| [Get Sorted Content](actions/get-sorted-content.md) | GET | Ranks supplied content in Pipeless Recommendations for a target object. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Pipeless Recommendations. |
| [Create Events Batch](actions/create-events-batch.md) | POST | Creates up to 10 events in Pipeless Recommendations. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes one or more events from Pipeless Recommendations. |
| [Get Recent Events](actions/get-recent-events.md) | GET | Retrieves recent events from Pipeless Recommendations. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Relationship Counts](actions/get-relationship-counts.md) | GET | Retrieves relationship counts for an object in Pipeless Recommendations. |
| [Get Relationship Exists](actions/get-relationship-exists.md) | GET | Checks whether a relationship exists in Pipeless Recommendations. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Related Tags](actions/get-related-tags.md) | GET | Retrieves related tags in Pipeless Recommendations. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Recommended Users To Follow](actions/get-recommended-users-to-follow.md) | GET | Retrieves recommended users to follow in Pipeless Recommendations. |
| [Get Related Users](actions/get-related-users.md) | GET | Retrieves related users in Pipeless Recommendations. |

