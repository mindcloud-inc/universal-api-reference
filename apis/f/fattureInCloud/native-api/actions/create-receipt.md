# Create Receipt with Fatture in Cloud

Creates a new receipt in Fatture in Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/c/:company_id/receipts`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Create Receipt](https://developers.fattureincloud.it/api-reference/#operation/createReceipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `data` | body | `object` | yes | The receipt payload inside the provider data envelope. |
