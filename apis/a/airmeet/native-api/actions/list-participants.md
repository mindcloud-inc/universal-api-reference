# List Participants with Airmeet

Finds participants in a specific Airmeet event.

## Endpoint

- **Method:** `GET`
- **Path:** `/airmeet/{airmeetId}/participants`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [List Participants](https://help.airmeet.com/support/solutions/articles/82000909768-1-event-details-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `emailIds` | query | `string` | no | One or more comma-separated participant email addresses to filter by. |
| `pageNumber` | query | `number` | no | Page number of participants to fetch. |
| `resultSize` | query | `number` | no | Maximum number of participants to return per page. |
| `sortingDirection` | query | `string` | no | Sort direction, typically ASC or DESC. |
| `sortingKey` | query | `string` | no | Participant sorting column such as name, email, or registrationDate. |
