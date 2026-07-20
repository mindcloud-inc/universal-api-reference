# List Memberships with Webex

Lists memberships in your Webex account.

## Endpoint

- **Method:** `GET`
- **Path:** `/memberships`
- **Base URL:** `https://webexapis.com/v1`
- **Official documentation:** [List Memberships](https://developer.webex.com/messaging/docs/api/v1/memberships/list-memberships)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `max` | query | `number` | no | Maximum number of memberships to return. |
| `roomId` | query | `string` | no | Filter memberships to one room. |
