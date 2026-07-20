# List LinkedIn Accounts with Hey Reach

Retrieves LinkedIn accounts from Hey Reach.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/li_account/GetAll`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [List LinkedIn Accounts](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offset` | body | `number` | no | Number of records to skip before returning results. |
| `keyword` | body | `string` | no | Optional account-name search keyword. |
| `limit` | body | `number` | no | Maximum number of LinkedIn accounts to return. |
