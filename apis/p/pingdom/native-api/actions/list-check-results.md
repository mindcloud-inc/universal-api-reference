# List Check Results with Pingdom

## Endpoint

- **Method:** `GET`
- **Path:** `/results/:checkid`
- **Base URL:** `https://api.pingdom.com/api/3.1`
- **Official documentation:** [List Check Results](https://docs.pingdom.com/api/#tag/Results)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkid` | path | `number` | yes | Identifier of the check. |
| `from` | query | `number` | no | Start of the results time range as UNIX time. |
| `to` | query | `number` | no | End of the results time range as UNIX time. |
| `probes` | query | `string` | no | Comma-separated list of probe identifiers. |
| `status` | query | `string` | no | Comma-separated list of result statuses. |
| `includeanalysis` | query | `boolean` | no | Include available root-cause analysis identifiers. |
| `maxresponse` | query | `number` | no | Maximum response time in milliseconds. |
| `minresponse` | query | `number` | no | Minimum response time in milliseconds. |
