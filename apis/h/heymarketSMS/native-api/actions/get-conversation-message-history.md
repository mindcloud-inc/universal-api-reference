# Get Conversation Message History with Heymarket SMS

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/messages`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Get Conversation Message History](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumber` | query | `string` | yes | Target phone number in E.164 format without the plus sign. |
| `inboxID` | query | `number` | yes | Unique identifier of the inbox. |
| `timestamp` | query | `number` | no | Latest time to search as a Unix timestamp. |
