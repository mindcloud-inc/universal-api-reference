# List Contacts with Odoo

Retrieves contacts from Odoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/res.partner/search_read`
- **Base URL:** `https://{domain}/json/2`
- **Official documentation:** [List Contacts](https://www.odoo.com/documentation/19.0/developer/reference/external_api.html)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | no | Optional Odoo domain filter JSON array, for example [["is_company","=",true]]. |
| `fields` | body | `string` | no | Optional array of fields to return. |
| `limit` | body | `number` | no | Maximum number of records to return. |
| `offset` | body | `number` | no | Number of records to skip before returning results. |
| `order` | body | `string` | no | Optional Odoo order clause, for example name asc. |
