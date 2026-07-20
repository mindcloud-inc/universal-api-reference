# Update Group with SMSGatewayCenter SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/SMSApi/group/update`
- **Base URL:** `https://unify.smsgateway.center`
- **Official documentation:** [Update Group](https://www.smsgatewaycenter.com/developer-api/update-group/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | ID of the SMSGatewayCenter group to update. |
| `groupname` | body | `string` | yes | New name for the SMSGatewayCenter contact group. |
