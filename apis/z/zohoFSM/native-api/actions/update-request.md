# Update Request with Zoho FSM

Updates an existing request in Zoho FSM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Requests/:recordId`
- **Base URL:** `{api_domain}/fsm/v1`
- **Official documentation:** [Update Request](https://www.zoho.com/fsm/developer/help/api/edit-request.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[].Summary` | body | `string` | yes | — |
| `recordId` | path | `string` | yes | The Zoho FSM record ID. |
| `data[].Contact` | body | `string` | yes | — |
| `data[].Company` | body | `string` | yes | — |
| `data[].Service_Address` | body | `object` | yes | The service address for the request. |
| `data[].Billing_Address` | body | `object` | yes | The billing address for the request. |
