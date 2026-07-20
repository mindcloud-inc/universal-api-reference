# Get all Viber Session Messages by a Phone Number with Routee

Retrieves all Viber session messages by a phone number from Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/viber/session`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Get all Viber Session Messages by a Phone Number](https://docs.routee.net/reference/get-all-viber-session-messages-by-a-phone-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | The page number to retrieve, default value is 0 (meaning the first page). |
| `size` | query | `number` | no | The number of items to retrieve, default value is 20. |
| `phoneNumber` | body | `string` | no | The phone number. Format with a '+' and country code e.g., +3069485xxxxx (E.164 format). |
| `dateStart` | query | `date` | no | The start date of the query. |
| `dateEnd` | query | `date` | no | The end date of the query. Sessions will be included in their whole even if they exceed the end date set by the user. We will never return sessions with missing messages. |
