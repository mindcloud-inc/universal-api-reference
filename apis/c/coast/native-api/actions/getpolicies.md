# Get All Policies with Coast

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/policies`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Get All Policies](https://coastpay.com/integrations/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nextPageToken` | query | `string` | no | A token that represents the next page of results. This token is returned in the response of a previous request and should be used to retrieve the next set of results. If not provided, the first page of results will be returned. |
| `pageSize` | query | `number` | no | The maximum number of results to return per page. If this parameter is not specified, the page size will be 10. This parameter works in conjunction with pagination tokens. |
| `archived` | query | `boolean` | no | Return archived responses |
| `type` | query | `list` | no | Return archived responses Accepted values: `0`, `1`. |
