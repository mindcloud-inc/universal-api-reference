# List Registration UTMs with Airmeet

Finds registration UTM data in Airmeet.

## Endpoint

- **Method:** `GET`
- **Path:** `/airmeet/{airmeetId}/utms`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [List Registration UTMs](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Fetch UTM registrations after this cursor. |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `before` | query | `string` | no | Fetch UTM registrations before this cursor. |
| `size` | query | `number` | no | Number of UTM registrations to return per page, between 1 and 50. |
