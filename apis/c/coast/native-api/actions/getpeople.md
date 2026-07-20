# Get All People with Coast

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/people`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Get All People](https://coastpay.com/integrations/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Return responses with email |
| `nextPageToken` | query | `string` | no | A token that represents the next page of results. This token is returned in the response of a previous request and should be used to retrieve the next set of results. If not provided, the first page of results will be returned. |
| `phoneNumber` | query | `string` | no | Return results with matching phone number |
| `pageSize` | query | `number` | no | The maximum number of results to return per page. If this parameter is not specified, the page size will be 10. This parameter works in conjunction with pagination tokens. |
| `active` | query | `boolean` | no | Return responses with active state |
| `departmentId` | query | `string` | no | Only return people assigned to this Coast department ID. |
| `locationId` | query | `string` | no | Only return people assigned to this Coast location ID. |
| `policyId` | query | `string` | no | Only return people assigned to this Coast policy ID. |
| `roleId` | query | `string` | no | Only return people assigned to this Coast role ID. |
