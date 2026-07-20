# Get Package Verification with SigningHub

Retrieves package verification details from SigningHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/packages/:packageId/verification`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Get Package Verification](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Package_GetVerification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | Package ID of the package to verify. |
