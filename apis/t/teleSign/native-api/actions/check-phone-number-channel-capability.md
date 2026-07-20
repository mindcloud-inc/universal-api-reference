# Check Phone Number Channel Capability with TeleSign

## Endpoint

- **Method:** `GET`
- **Path:** `/capability/{channel}/{phone_number}`
- **Base URL:** `https://rest-ww.telesign.com`
- **Official documentation:** [Check Phone Number Channel Capability](https://developer.telesign.com/enterprise/reference/checkphonenumberchannelcapability)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | path | `string` | yes | The messaging channel to evaluate for the phone number. |
| `phone_number` | path | `string` | yes | The destination phone number in E.164 format. |
