# List Screenshots with PeekShot

Retrieves screenshots from PeekShot with optional filtering.

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshots`
- **Base URL:** `https://api.peekshot.com/api/v1`
- **Official documentation:** [List Screenshots](https://docs.peekshot.com/api-reference/get-screenshots-list-m4vc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | query | `string` | no | Filter by project ID. |
| `url` | query | `string` | no | Filter by captured URL. |
| `status` | query | `string` | no | Filter by screenshot status: PENDING, COMPLETE, or FAILED. |
| `page` | query | `string` | no | Page number for paginated results. |
| `limit` | query | `string` | no | Number of results per page. |
