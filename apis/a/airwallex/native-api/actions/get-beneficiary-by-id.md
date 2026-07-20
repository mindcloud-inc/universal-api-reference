# Get Beneficiary by ID with Airwallex

Retrieves a beneficiary by ID from Airwallex.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/beneficiaries/{{beneficiaryId}}`
- **Base URL:** `https://api-demo.airwallex.com`
- **Official documentation:** [Get Beneficiary by ID](https://www.airwallex.com/docs/payouts/beneficiaries/retrieve-beneficiaries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `beneficiaryId` | path | `string` | yes | The Airwallex beneficiary ID to retrieve. |
