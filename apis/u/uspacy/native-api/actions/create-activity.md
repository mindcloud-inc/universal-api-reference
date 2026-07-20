# Create Activity with Uspacy

Creates a new activity in Uspacy.

## Endpoint

- **Method:** `POST`
- **Path:** `/activities/v1/activities`
- **Base URL:** `https://{site}`
- **Official documentation:** [Create Activity](https://uspacy.readme.io/reference/post_activities-v1-activities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The activity title. |
| `start_time` | body | `number` | yes | The activity start timestamp. |
| `end_time` | body | `number` | yes | The activity end timestamp. |
