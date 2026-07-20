# Delete Contact with SMSGatewayCenter SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/SMSApi/contact/delete`
- **Base URL:** `https://unify.smsgateway.center`
- **Official documentation:** [Delete Contact](https://www.smsgatewaycenter.com/developer-api/delete-contact/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | ID of the SMSGatewayCenter contact to delete. |
