# List Deals with Karma CRM

Retrieves a list of deals from Karma CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/deals.json`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [List Deals](https://docs.karmacrm.com/#get-all-deals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to retrieve. |
| `since` | query | `date` | no | Filter deals updated after a specified date. |
