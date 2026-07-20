# Get Thread Details with Lodgify

Retrieves message thread details from Lodgify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/messaging/:threadUid`
- **Base URL:** `https://api.lodgify.com`
- **Official documentation:** [Get Thread Details](https://docs.lodgify.com/reference/get_v2-messaging-threadguid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `threadUid` | path | `string` | yes | Reservation thread UID from the booking details. |
