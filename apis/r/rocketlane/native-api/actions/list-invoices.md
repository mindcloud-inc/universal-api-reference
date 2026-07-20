# List Invoices with Rocketlane

Lists invoices in Rocketlane.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.0/invoices`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [List Invoices](https://developer.rocketlane.com/reference/search-invoices)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeFields` | query | `list<string>` | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | query | `boolean` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `match` | query | `string` | no | You can use the match param to specify if we need to filter the entries using either AND(all) / OR(any). Defaults to AND. |
