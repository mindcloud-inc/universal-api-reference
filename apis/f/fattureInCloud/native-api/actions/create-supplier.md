# Create Supplier with Fatture in Cloud

Creates a new supplier in Fatture in Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/c/:company_id/entities/suppliers`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Create Supplier](https://developers.fattureincloud.it/api-reference/#operation/createSupplier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `data` | body | `object` | yes | The supplier payload inside the provider data envelope. |
