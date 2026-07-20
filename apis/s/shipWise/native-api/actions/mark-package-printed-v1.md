# Mark Package Printed V1 with ShipWise

Updates a package to printed status in ShipWise.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Print/:PackageId/MarkPrinted`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [Mark Package Printed V1](https://api.shipwise.com/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PackageId` | path | `string` | yes | ShipWise package ID. |
