# Get Tickets with Wrangle

## Endpoint

- **Method:** `GET`
- **Path:** `/inboxes/:inboxId/tickets`
- **Base URL:** `https://slack.wrangle.io/api/v1`
- **Official documentation:** [Get Tickets](https://wrangle.apidocumentation.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboxId` | path | `string` | yes | The Wrangle inbox ID. |
| `page` | query | `number` | no | Page number for pagination (1-based). Defaults to 1. |
| `pageSize` | query | `number` | no | Number of tickets per page. Maximum 200. Defaults to 200. |
