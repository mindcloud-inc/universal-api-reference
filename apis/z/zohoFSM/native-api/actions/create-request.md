# Create Request with Zoho FSM

Creates a new request in Zoho FSM.

## Endpoint

- **Method:** `POST`
- **Path:** `/Requests`
- **Base URL:** `{api_domain}/fsm/v1`
- **Official documentation:** [Create Request](https://www.zoho.com/fsm/developer/help/api/create-request.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[].Summary` | body | `string` | yes | — |
| `data[].Contact` | body | `string` | yes | — |
| `data[].Company` | body | `string` | yes | — |
| `data[].Service_Address` | body | `object` | yes | The service address for the request. |
| `data[].Billing_Address` | body | `object` | yes | The billing address for the request. |
