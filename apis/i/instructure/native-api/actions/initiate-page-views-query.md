# Initiate Page Views Query with Instructure

Initiates a page views query in Instructure Canvas.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/self/page_views/query`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Initiate Page Views Query](https://developerdocs.instructure.com/services/canvas/resources/users#method.page_views.query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | body | `string` | yes | End date for the query. |
| `results_format` | body | `string` | yes | Requested results format. |
| `start_date` | body | `string` | yes | Start date for the query. |
