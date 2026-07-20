# Update Contact with SMSGatewayCenter SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/SMSApi/contact/update`
- **Base URL:** `https://unify.smsgateway.center`
- **Official documentation:** [Update Contact](https://www.smsgatewaycenter.com/developer-api/update-contact/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | ID of the SMSGatewayCenter contact to update. |
| `contactname` | body | `string` | yes | Updated display name for the contact. |
| `mobileno` | body | `string` | yes | Updated mobile number for the contact. |
| `groupid` | body | `string` | yes | Updated SMSGatewayCenter group ID for the contact. |
