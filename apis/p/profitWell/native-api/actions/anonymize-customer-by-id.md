# Anonymize Customer By ID with ProfitWell

Anonymizes a customer in ProfitWell by customer ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/gdpr/anonymize_by_customer_id/:customer_id/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Anonymize Customer By ID](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The data-provider specific customer ID. |
