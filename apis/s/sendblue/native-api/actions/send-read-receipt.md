# Send Read Receipt with Sendblue

Sends a read receipt through Sendblue.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/mark-read`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Send Read Receipt](https://docs.sendblue.com/api-v2/read-receipts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | yes | The conversation phone number to mark as read in E.164 format. |
| `from_number` | body | `string` | yes | Your Sendblue line number in E.164 format. |
