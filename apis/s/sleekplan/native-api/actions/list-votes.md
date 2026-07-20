# List Votes with Sleekplan

## Endpoint

- **Method:** `GET`
- **Path:** `/post/:postid/votes`
- **Base URL:** `https://api.sleekplan.com/v1`
- **Official documentation:** [List Votes](https://sleekplan.com/docs/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filter` | query | `string` | no |
| `postid` | path | `string` | yes |
| `sort` | query | `string` | no |
