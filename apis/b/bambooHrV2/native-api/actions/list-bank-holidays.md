# List Bank Holidays with BambooHR

Lists bank holidays from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/meta/bank-holidays`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Bank Holidays](https://documentation.bamboohr.com/reference/list-bank-holidays)

## Requirements

- **OAuth scopes:** `meta`
- **scope:** `meta` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | When set, only holidays whose dates fall in this calendar year are returned. When omitted, all bank holidays are returned. Values outside 1-9999 return 422. |
