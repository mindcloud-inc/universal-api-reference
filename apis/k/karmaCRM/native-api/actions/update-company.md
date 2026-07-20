# Update Company with Karma CRM

Updates an existing company in Karma CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v3/companies/:id.json`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [Update Company](https://docs.karmacrm.com/#update-a-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the company to update. |
| `company` | body | `object` | yes | Company payload object with the fields to update. |
