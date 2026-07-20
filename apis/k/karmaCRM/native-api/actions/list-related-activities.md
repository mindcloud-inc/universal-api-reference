# List Related Activities with Karma CRM

Retrieves activities related to a contact in Karma CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/activities/related.json`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [List Related Activities](https://docs.karmacrm.com/#get-related-activities-for-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to retrieve. |
| `per_page` | query | `number` | no | Number of activities per page. |
| `record_id` | query | `number` | yes | The related record ID. |
