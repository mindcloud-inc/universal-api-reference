# Anonymize Customer By Email with ProfitWell

Anonymizes a customer in ProfitWell by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/gdpr/anonymize_by_email/:email/`
- **Base URL:** `https://api.profitwell.com`
- **Official documentation:** [Anonymize Customer By Email](https://classic.paddle.com/profitwell/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | The customer email. |
