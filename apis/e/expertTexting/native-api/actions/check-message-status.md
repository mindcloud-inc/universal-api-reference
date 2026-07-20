# Check Message Status with ExpertTexting

Retrieves message status from ExpertTexting by message ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/ExptRestApi/sms/json/Message/Status`
- **Base URL:** `https://www.experttexting.com`
- **Official documentation:** [Check Message Status](https://www.experttexting.com/appv2/Documentation/Status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | query | `string` | yes | ExpertTexting message ID to check. |
