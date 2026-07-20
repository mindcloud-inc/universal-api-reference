# List Persons with Leadspicker

Retrieves persons from Leadspicker.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/sb/api/persons-simple`
- **Base URL:** `https://app.leadspicker.com`
- **Official documentation:** [List Persons](https://app.leadspicker.com/app/sb/api/docs#/Person/apps_salesbooster_api_persons_simple)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | yes | Project identifier whose persons should be listed. |
| `page` | query | `number` | no | Page number for persons. |
| `page_size` | query | `number` | no | Number of persons per page. |
| `query` | query | `string` | no | Search persons. |
| `order_by` | query | `list<string>` | no | Sort persons by created or -created. Accepted values: `0`, `1`. |
