# Delete Group with SMSGatewayCenter SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/SMSApi/group/delete`
- **Base URL:** `https://unify.smsgateway.center`
- **Official documentation:** [Delete Group](https://www.smsgatewaycenter.com/developer-api/delete-group/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | ID of the SMSGatewayCenter group to delete. |
