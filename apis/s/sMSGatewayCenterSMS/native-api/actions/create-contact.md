# Create Contact with SMSGatewayCenter SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/SMSApi/contact/create`
- **Base URL:** `https://unify.smsgateway.center`
- **Official documentation:** [Create Contact](https://www.smsgatewaycenter.com/developer-api/create-contact/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactname` | body | `string` | yes | Display name for the SMSGatewayCenter contact. |
| `mobileno` | body | `string` | yes | Mobile number for the contact. |
| `groupid` | body | `string` | yes | Target SMSGatewayCenter group ID for the contact. |
