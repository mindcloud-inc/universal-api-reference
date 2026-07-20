# Advanced People Search with JustSift

## Endpoint

- **Method:** `POST`
- **Path:** `/search/people`
- **Base URL:** `https://api.justsift.com/v1`
- **Official documentation:** [Advanced People Search](https://developers.justsift.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | body | `string` | no | Generic term searched across searchable Sift fields. |
| `page` | body | `number` | no | Page number to retrieve. Sift pages start at 1. |
| `pageSize` | body | `number` | no | Number of people to return, from 0 to 100. |
| `sortBy` | body | `string` | no | Sift field objectKey to sort by. |
| `sortDirection` | body | `string` | no | Sort direction, asc or desc. Accepted values: `0`, `1`. |
| `filter` | body | `object` | no | Advanced Sift PeopleFilters object using and, or, not, or field comparison clauses. |
