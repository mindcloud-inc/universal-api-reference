# Get User Detail with Kommunicate

Retrieves user details from Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/user/v2/detail`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Get User Detail](https://docs.kommunicate.io/docs/api-detail#get-user-detail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userIdList[]` | body | `array<string>` | yes | List of Kommunicate user IDs to retrieve. |
| `fetchLatestMessageTime` | query | `boolean` | no | Include each user's latest message timestamp in the response when true. |
