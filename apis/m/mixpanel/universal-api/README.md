# <img src="https://images.mindcloud.co/apps/icons/mixpanel_1773345485957.png" alt="Mixpanel logo" width="28" height="28"> Mixpanel: Universal API

Analyze product usage, manage cohorts, and export analytics data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mixpanel/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mixpanel.com
- **Vendor API docs:** https://developer.mixpanel.com/reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Export Events](actions/export-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/export-events?connectionId=$CONNECTION_ID&fromDate=string&toDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile Event Activity](actions/get-profile-event-activity.md) | GET | Retrieves profile event activity from Mixpanel. |

### Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Create Annotation](actions/create-annotation.md) | POST | Creates a new annotation in Mixpanel. |
| [Delete Annotation](actions/delete-annotation.md) | DELETE | Deletes an existing annotation from Mixpanel. |
| [Get Annotation](actions/get-annotation.md) | GET | Retrieves an annotation from Mixpanel. |
| [List Annotations](actions/list-annotations.md) | GET | Retrieves annotations from a Mixpanel project. |
| [Update Annotation](actions/update-annotation.md) | PUT | Updates an existing annotation in Mixpanel. |

### Cohort

| Action | Method | Description |
| --- | --- | --- |
| [List Saved Cohorts](actions/list-saved-cohorts.md) | GET | Retrieves saved cohorts from Mixpanel. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Export Events](actions/export-events.md) | GET | Retrieves raw events from Mixpanel. |
| [List Today's Top Events](actions/list-todays-top-events.md) | GET | Retrieves today's top events from Mixpanel. |
| [List Top Event Properties](actions/list-top-event-properties.md) | GET | Retrieves top event properties from Mixpanel. |
| [List Top Event Property Values](actions/list-top-event-property-values.md) | GET | Retrieves top event property values from Mixpanel. |
| [List Top Events](actions/list-top-events.md) | GET | Retrieves top events from Mixpanel. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Import Events](actions/import-events.md) | POST | Creates new events in Mixpanel. |
| [Track Events](actions/track-events.md) | POST | Creates new tracked events in Mixpanel. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Batch Update Group Profiles](actions/batch-update-group-profiles.md) | PUT | Updates multiple group profiles in Mixpanel. |
| [Delete Group Property](actions/delete-group-property.md) | PUT | Deletes a group property from Mixpanel. |
| [Remove from Group List Property](actions/remove-from-group-list-property.md) | PUT | Removes values from a group list in Mixpanel. |
| [Set Group Property Once](actions/set-group-property-once.md) | PUT | Sets a group property once in Mixpanel. |
| [Union Group List Property](actions/union-group-list-property.md) | PUT | Unions values into a group list in Mixpanel. |
| [Update Group Property](actions/update-group-property.md) | PUT | Updates a group property in Mixpanel. |

### Identity

| Action | Method | Description |
| --- | --- | --- |
| [Create Alias](actions/create-alias.md) | POST | Creates a user identity alias in Mixpanel. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Query Profiles](actions/query-profiles.md) | GET | Retrieves profiles from Mixpanel. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Query Funnel Report](actions/query-funnel-report.md) | GET | Retrieves a funnel report from Mixpanel. |
| [Query Retention Report](actions/query-retention-report.md) | GET | Retrieves a retention report from Mixpanel. |
| [Query Saved Insights Report](actions/query-saved-insights-report.md) | GET | Retrieves a saved insights report from Mixpanel. |
| [Query Segmentation Report](actions/query-segmentation-report.md) | GET | Retrieves a segmentation report from Mixpanel. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Append to Profile List Property](actions/append-to-profile-list-property.md) | PUT | Appends values to a user profile list in Mixpanel. |
| [Delete Profile Property](actions/delete-profile-property.md) | PUT | Deletes a user profile property from Mixpanel. |
| [Increment Profile Numerical Property](actions/increment-profile-numerical-property.md) | PUT | Increments a user profile number property in Mixpanel. |
| [Remove from Profile List Property](actions/remove-from-profile-list-property.md) | PUT | Removes values from a user profile list in Mixpanel. |
| [Set Profile Property](actions/set-profile-property.md) | PUT | Updates a user profile property in Mixpanel. |
| [Set Profile Property Once](actions/set-profile-property-once.md) | PUT | Sets a user profile property once in Mixpanel. |
| [Union Profile List Property](actions/union-profile-list-property.md) | PUT | Unions values into a user profile list in Mixpanel. |
| [Update Multiple Profiles](actions/update-multiple-profiles.md) | PUT | Updates multiple user profiles in Mixpanel. |

