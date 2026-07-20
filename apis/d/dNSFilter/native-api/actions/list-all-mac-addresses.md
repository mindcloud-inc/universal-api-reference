# List All MAC Addresses with DNSFilter

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/mac_addresses/all`
- **Base URL:** `https://api.dnsfilter.com`
- **Official documentation:** [List All MAC Addresses](https://api.dnsfilter.com/docs#/paths/~1v1~1mac_addresses~1all/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_ids` | query | `number<number>` | no | Organization IDs, defaults to user organization ID Send multiple values as a array separated by `,`. |
