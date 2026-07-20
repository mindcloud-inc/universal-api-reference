# List Policies with DNSFilter

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/policies`
- **Base URL:** `https://api.dnsfilter.com`
- **Official documentation:** [List Policies](https://api.dnsfilter.com/docs#/paths/~1v1~1policies/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `number` | no | Organization ID |
| `include_global_policies` | query | `boolean` | no | Include global policies |
