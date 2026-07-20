# Get Page Views Query Status with Instructure

Retrieves page views query status from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/self/page_views/query/:query_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Get Page Views Query Status](https://developerdocs.instructure.com/services/canvas/resources/users#method.page_views.show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query_id` | path | `string` | yes | Page views query ID. |
