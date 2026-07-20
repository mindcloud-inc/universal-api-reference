# List Conversations with Rocketlane

Lists conversations in Rocketlane.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.0/conversations`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [List Conversations](https://developer.rocketlane.com/reference/get-all-conversations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeFields` | query | `list<string>` | no | Use this query parameter to opt in for fields to be returned in the response body. Use comma separated values to fetch the respective fields. If left blank, default properties are returned. |
| `includeAllFields` | query | `boolean` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
