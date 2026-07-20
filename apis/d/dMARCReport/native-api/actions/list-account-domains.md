# List Account Domains with DMARC Report

Retrieves domain accounts from a DMARC Report account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/domain_accounts`
- **Base URL:** `https://api.dmarcreport.com/v2`
- **Official documentation:** [List Account Domains](https://docs.dmarcreport.com/api/2.0.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | DMARC Report account identifier from the endpoint path. |
