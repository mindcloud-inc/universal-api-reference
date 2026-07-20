# Get Contact-to-Company Interaction Graph with SigParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Contacts/CompaniesGraph`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [Get Contact-to-Company Interaction Graph](https://ipaas.sigparser.com/v1#post-api-contacts-companiesgraph)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_email` | body | `string` | yes | Email address of the primary contact. |
| `related_company_domain` | body | `string` | yes | Domain of the related company. |
| `start_date` | body | `date` | yes | Start date of the interactions. |
