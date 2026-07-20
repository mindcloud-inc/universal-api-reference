# Create Verification Campaign with Wbiztool

Creates a WhatsApp number verification campaign in Wbiztool.

## Endpoint

- **Method:** `POST`
- **Path:** `/verification/create/`
- **Base URL:** `https://wbiztool.com/api/v1`
- **Official documentation:** [Create Verification Campaign](https://wbiztool.com/docs/verification-create-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numbers[]` | body | `array<string>` | yes | Phone numbers to verify as an array. |
| `campaign_name` | body | `string` | no | Optional label for the verification campaign. |
