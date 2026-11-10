# List Deposits with ServiceTitan

Retrieves bank deposits and their accounting details from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `accounting/v2/tenant/{tenant}/bank-deposits`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Deposits](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/Deposits_GetList)

## Requirements

- **scope:** `tn.acc.bankdeposits:r` — Requires Accounting → Bank Deposits read access in ServiceTitan.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Deposit IDs to retrieve, up to 50 IDs. Send multiple values as a string separated by `,`. |
| `modifiedBefore` | query | `date` | no | — |
| `modifiedOnOrAfter` | query | `date` | no | — |
| `createdBefore` | query | `date` | no | — |
| `createdOnOrAfter` | query | `date` | no | — |
| `depositDateBefore` | query | `date` | no | — |
| `depositDateOnOrAfter` | query | `date` | no | — |
| `reviewedBefore` | query | `date` | no | — |
| `reviewedOnOrAfter` | query | `date` | no | — |
| `reviewStatus` | query | `list<string>` | no | Accepted values: `NeedsReview`, `Reviewed`. |
| `depositStatus` | query | `list<string>` | no | Accepted values: `Deposited`, `Open`, `Undefined`. |
| `syncStatus` | query | `list<string>` | no | Accepted values: `Exported`, `Pending`, `Posted`. |
| `grossAmountGreater` | query | `number` | no | — |
| `grossAmountLess` | query | `number` | no | — |
| `includeTotal` | query | `boolean` | no | — |
| `sort` | query | `string` | no | Prefix a supported field name with + for ascending order or - for descending order. |
