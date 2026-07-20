# Search People with JustSift

## Endpoint

- **Method:** `GET`
- **Path:** `/search/people`
- **Base URL:** `https://api.justsift.com/v1`
- **Official documentation:** [Search People](https://developers.justsift.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Generic term searched across searchable Sift fields. |
| `page` | query | `number` | no | Page number to retrieve. Sift pages start at 1. |
| `pageSize` | query | `number` | no | Number of people to return, from 0 to 100. |
| `sortBy` | query | `string` | no | Sift field objectKey to sort by. |
| `sortDirection` | query | `string` | no | Sort direction, asc or desc. Accepted values: `0`, `1`. |
| `orQuery` | query | `boolean` | no | When true, uses OR for provided filters instead of AND. |
