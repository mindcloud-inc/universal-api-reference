# List Calls with Callingly

Retrieves calls from Callingly.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/calls`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [List Calls](https://help.callingly.com/article/38-callingly-api-documentation#list-calls)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start` | query | `string` | no |
| `end` | query | `string` | no |
| `team_id` | query | `number` | no |
