# List Comments with Rocketlane

Lists comments in Rocketlane.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.0/comments`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [List Comments](https://developer.rocketlane.com/reference/get-comments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sourceType` | query | `string` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `includeAllFields` | query | `boolean` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `match` | query | `string` | no | You can use the match param to specify if we need to filter the entries using either AND(all) / OR(any). Defaults to AND. |
| `includeFields` | query | `list<string>` | no | Use this query parameter to opt in for fields to be returned in the response body. Use comma separated values to fetch the respective fields. If left blank, default properties are returned. |
