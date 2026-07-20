# List All Change Notifications with PagePixels

## Endpoint

- **Method:** `GET`
- **Path:** `/change_notifications`
- **Base URL:** `https://api.pagepixels.com`
- **Official documentation:** [List All Change Notifications](https://pagepixels.com/app/screenshots-api-documentation#show-all-changes-all)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | The result page to retrieve. |
| `limit` | query | `number` | no | The number of records to retrieve. |
| `after` | query | `number` | no | Only include records created after this unix timestamp. |
| `before` | query | `number` | no | Only include records created before this unix timestamp. |
| `order` | query | `string` | no | Sort order, either ASC or DESC. |
