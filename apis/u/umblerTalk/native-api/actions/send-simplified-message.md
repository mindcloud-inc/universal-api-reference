# Send Simplified Message with Umbler Talk

Creates a simplified message in Umbler Talk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/simplified/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Send Simplified Message](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromPhone` | body | `string` | yes | Sender/channel phone number. |
| `message` | body | `string` | no | Message text. |
| `organizationId` | body | `string` | yes | The organization ID. |
| `toPhone` | body | `string` | yes | Recipient phone number with area code. |
