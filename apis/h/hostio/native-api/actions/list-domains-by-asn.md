# List Domains by ASN with Host.io

Finds domains in Host.io by ASN.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/asn/:value`
- **Base URL:** `https://host.io/api`
- **Official documentation:** [List Domains by ASN](https://host.io/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | path | `string` | yes | ASN to search domains by. |
