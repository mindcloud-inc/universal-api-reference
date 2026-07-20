# List LinkedIn Accounts with Salesrobot

## Endpoint

- **Method:** `GET`
- **Path:** `/api/linkedinAccounts`
- **Base URL:** `https://api.boomtechinc.com`
- **Official documentation:** [List LinkedIn Accounts](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchTerm` | query | `string` | no | Filter LinkedIn accounts by a search string. |
| `linkedinAccountUuid` | query | `string` | no | Optionally scope the response to one LinkedIn account UUID. |
