# Get Transfer by ID with Airwallex

Retrieves a transfer by ID from Airwallex.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/transfers/{{transferId}}`
- **Base URL:** `https://api-demo.airwallex.com`
- **Official documentation:** [Get Transfer by ID](https://www.airwallex.com/docs/payouts/transfers/create-a-transfer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transferId` | path | `string` | yes | The Airwallex transfer ID to retrieve. |
