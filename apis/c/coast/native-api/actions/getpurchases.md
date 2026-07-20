# Get All Purchases with Coast

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/transactions/purchases`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Get All Purchases](https://coastpay.com/integrations/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nextPageToken` | query | `string` | no | A token that represents the next page of results. Use the token returned by a previous response to retrieve the next page of purchases. |
| `pageSize` | query | `number` | no | The maximum number of purchases to return per page. |
| `status` | query | `list` | no | Only return purchases with this status. Accepted values: `0`, `1`, `2`. |
| `completedStartingAt` | query | `string` | no | Only return purchases completed on or after this date. |
| `completedEndingBefore` | query | `string` | no | Only return purchases completed before this date. |
| `createdStartingAt` | query | `string` | no | Only return purchases created on or after this date. |
| `createdEndingBefore` | query | `string` | no | Only return purchases created before this date. |
| `assignedPersonId` | query | `string` | no | Only return purchases assigned to this Coast person ID. |
| `assignedPersonDepartmentId` | query | `string` | no | Only return purchases whose assigned person belongs to this Coast department ID. |
| `assignedPersonLocationId` | query | `string` | no | Only return purchases whose assigned person belongs to this Coast location ID. |
| `assignedPersonPolicyId` | query | `string` | no | Only return purchases whose assigned person uses this Coast policy ID. |
| `assignedVehicleId` | query | `string` | no | Only return purchases assigned to this Coast vehicle ID. |
| `assignedVehicleDepartmentId` | query | `string` | no | Only return purchases whose assigned vehicle belongs to this Coast department ID. |
| `assignedVehicleLocationId` | query | `string` | no | Only return purchases whose assigned vehicle belongs to this Coast location ID. |
| `assignedVehiclePolicyId` | query | `string` | no | Only return purchases whose assigned vehicle uses this Coast policy ID. |
| `cardId` | query | `string` | no | Only return purchases made with this Coast card ID. |
| `merchantLocationId` | query | `string` | no | Only return purchases from this Coast merchant location ID. |
| `merchantBrandId` | query | `string` | no | Only return purchases from this Coast merchant brand ID. |
