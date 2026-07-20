# Update a Company with Beebole

Updates an existing company in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Update a Company](https://beebole.com/help/api#update-a-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company.id` | body | `number` | yes | The Beebole company ID to update. |
| `company.name` | body | `string` | no | Updated company name. |
