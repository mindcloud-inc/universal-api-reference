# Unblock Attendee with Airmeet

Restores attendee access in a specific Airmeet.

## Endpoint

- **Method:** `PUT`
- **Path:** `/airmeet/{airmeetId}/attendee/unblock`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [Unblock Attendee](https://help.airmeet.com/support/solutions/articles/82000909769-2-manage-registrations-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `attendeeEmail` | body | `string` | yes | The email address of the attendee to unblock. |
