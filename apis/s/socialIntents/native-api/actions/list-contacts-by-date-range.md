# List Contacts By Date Range with Social Intents

Retrieves contacts from Social Intents using a date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://www.socialintents.com/v1/api`
- **Official documentation:** [List Contacts By Date Range](https://www.socialintents.com/docs/integrations/rest-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_from` | query | `string` | yes | Start date for contact filtering. |
| `date_to` | query | `string` | yes | End date for contact filtering. |
