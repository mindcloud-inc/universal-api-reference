# Create Activity with Ellipsend

Creates a new activity in Ellipsend.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.ellipsend.com/v1/activity`
- **Base URL:** `https://api.ellipsend.com/v1`
- **Official documentation:** [Create Activity](https://api.ellipsend.com/v1/docs#/Activity/post_v1_activity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | body | `string` | yes | The Ellipsend token. |
| `activity_type_id` | body | `number` | yes | The activity type ID. |
| `fields` | body | `object` | yes | Key/value pairs of fields for the activity. |
