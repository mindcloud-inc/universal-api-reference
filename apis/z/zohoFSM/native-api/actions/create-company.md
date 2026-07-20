# Create Company with Zoho FSM

Creates a new company in Zoho FSM.

## Endpoint

- **Method:** `POST`
- **Path:** `/Companies`
- **Base URL:** `{api_domain}/fsm/v1`
- **Official documentation:** [Create Company](https://www.zoho.com/fsm/developer/help/api/create-company.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[0].Company_Name` | body | `string` | yes | The name of the company. |
