# Create a Company with Beebole

Creates a new company in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Create a Company](https://beebole.com/help/api#create-a-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company.name` | body | `string` | yes | Name for the company to create. |
| `company.corporate` | body | `boolean` | no | Whether the company is corporate instead of a customer. |
