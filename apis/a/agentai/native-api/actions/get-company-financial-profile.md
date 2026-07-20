# Get Company Financial Profile with Agent.ai

Retrieves company financial profiles from Agent.ai by stock symbol.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/company_financial_profile`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Get Company Financial Profile](https://docs.agent.ai/api-reference/get-data/get-company-financial-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | yes | Stock symbol or symbols to retrieve financial profiles for. |
