# List Forms with Checkout Page

Retrieves forms from Checkout Page.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/forms/`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [List Forms](https://checkoutpage.com/docs/api/v1/forms/list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | The number of results per page. Minimum value is 1 and maximum is 100. Defaults to 20. |
| `starting_after` | query | `string` | no | A cursor value specifying the id of a resource to start before. Retrieves items that appear after this cursor in the list. Cannot be used together with `ending_before`. |
| `ending_before` | query | `string` | no | A cursor value specifying the id of a resource to end after. Retrieves items that appear before this cursor in the list. Cannot be used together with `starting_after`. |
| `status` | query | `string` | no | Filter forms by publication status. |
| `search` | query | `string` | no | Case-insensitive search matched against page name and title. |
