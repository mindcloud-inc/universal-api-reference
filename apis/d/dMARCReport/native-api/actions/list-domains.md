# List Domains with DMARC Report

Retrieves domains from a DMARC Report account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/domains.json`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [List Domains](https://docs.dmarcreport.com/api/2.0.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
