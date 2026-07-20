# List Groups with Growby

Retrieves groups from Growby.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [List Groups](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to fetch. |
| `pageSize` | query | `number` | no | Number of groups to return per page. |
| `sortBy` | query | `string` | no | Column to sort the results by. |
| `sortOrder` | query | `string` | no | Sort direction, such as ASC or DESC. |
