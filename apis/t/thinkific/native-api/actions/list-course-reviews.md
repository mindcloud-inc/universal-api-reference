# List Course Reviews with Thinkific

Retrieves course review records from Thinkific.

## Endpoint

- **Method:** `GET`
- **Path:** `/course_reviews`
- **Base URL:** `https://api.thinkific.com/api/public/v1`
- **Official documentation:** [List Course Reviews](https://developers.thinkific.com/api/api-documentation#/paths/~1course_reviews/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `approved` | query | `boolean` | no | When true, returns only approved course reviews. |
| `course_id` | query | `number` | yes | Course ID to filter course reviews. |
