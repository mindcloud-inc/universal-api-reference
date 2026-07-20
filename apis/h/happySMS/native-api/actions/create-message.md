# Create Message with Happy SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/protected/domain/sms/messages`
- **Base URL:** `https://www.api.nc`
- **Official documentation:** [Create Message](https://www.happy.nc/docs/sms.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | Recipient phone number in +687XXXXXX format. |
| `from` | body | `string` | no | Sender phone number. Optional when the API key already defines the sender. |
| `priority` | body | `string` | yes | SMS priority: LOW or HIGH. |
| `timeToLive` | body | `string` | no | ISO 8601 expiration timestamp for the SMS. |
| `message` | body | `string` | yes | SMS body content. |
| `externalId` | body | `string` | no | Optional caller-defined identifier. |
