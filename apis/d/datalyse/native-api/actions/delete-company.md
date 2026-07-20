# Delete Company with Datalyse

Deletes an existing company from Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/companies/delete.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Delete Company](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_lead_id` | body | `string` | yes | ID of the company to delete |
