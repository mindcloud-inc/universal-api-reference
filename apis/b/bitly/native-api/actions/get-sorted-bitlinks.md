# Get Sorted Bitlinks with Bitly

Retrieves sorted bitlinks for a group in Bitly.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_guid/bitlinks/:sort`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Get Sorted Bitlinks](https://dev.bitly.com/api-reference#getSortedBitlinks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `group_guid` | path | `string` | yes |
| `size` | query | `number` | no |
| `sort` | path | `string` | yes |
