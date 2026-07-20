# List Comments with Sleekplan

## Endpoint

- **Method:** `GET`
- **Path:** `/post/:postid/comments`
- **Base URL:** `https://api.sleekplan.com/v1`
- **Official documentation:** [List Comments](https://sleekplan.com/docs/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `postid` | path | `string` | yes |
| `sort` | query | `string` | no |
