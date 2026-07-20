# Get Unread Count with Beamer

Retrieves the unread post count from Beamer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/unread/count`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [Get Unread Count](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Segment filter used to match posts for the user. |
| `dateFrom` | query | `date` | no | Only count posts published on or after this date and time. |
| `userId` | query | `string` | no | Unique identifier for the user in your own app. |
| `userFirstName` | query | `string` | no | First name to include in the generated feed URL context. |
| `userLastName` | query | `string` | no | Last name to include in the generated feed URL context. |
| `userEmail` | query | `string` | no | Email address to include in the generated feed URL context. |
