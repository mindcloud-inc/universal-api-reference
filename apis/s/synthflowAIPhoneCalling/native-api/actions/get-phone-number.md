# Get Phone Number with Synthflow AI Phone Calling

Retrieves a phone number from Synthflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/numbers/:phone_number_slug`
- **Base URL:** `https://api.synthflow.ai/v2`
- **Official documentation:** [Get Phone Number](https://docs.synthflow.ai/api-reference/platform-api/phone-numbers/get-phone-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone_number_slug` | path | `string` | yes | The phone number slug without the leading plus sign. |
