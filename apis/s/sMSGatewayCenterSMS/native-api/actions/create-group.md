# Create Group with SMSGatewayCenter SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/SMSApi/group/create`
- **Base URL:** `https://unify.smsgateway.center`
- **Official documentation:** [Create Group](https://www.smsgatewaycenter.com/developer-api/create-group/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupname` | body | `string` | yes | Name of the SMSGatewayCenter contact group to create. |
