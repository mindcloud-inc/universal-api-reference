# Get All Vehicles with Coast

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/vehicles`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Get All Vehicles](https://coastpay.com/integrations/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nextPageToken` | query | `string` | no | A token that represents the next page of results. Use the token returned by a previous response to retrieve the next page of vehicles. |
| `pageSize` | query | `number` | no | The maximum number of vehicles to return per page. |
| `active` | query | `boolean` | no | Only return vehicles with this active status. |
| `departmentId` | query | `string` | no | Only return vehicles assigned to this Coast department ID. |
| `locationId` | query | `string` | no | Only return vehicles assigned to this Coast location ID. |
| `policyId` | query | `string` | no | Only return vehicles assigned to this Coast policy ID. |
