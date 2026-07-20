# List All Applications with DNSFilter

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/applications/all`
- **Base URL:** `https://api.dnsfilter.com`
- **Official documentation:** [List All Applications](https://api.dnsfilter.com/docs#/paths/~1v1~1applications~1all/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_ids` | query | `number<number>` | no | Category IDs, defaults to all Send multiple values as a array separated by `,`. |
