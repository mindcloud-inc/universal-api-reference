# Get Company Earnings Info with Agent.ai

Retrieves company earnings information from Agent.ai by stock symbol.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/company_financial_info`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Get Company Earnings Info](https://docs.agent.ai/api-reference/get-data/get-company-earnings-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | yes | Stock symbol of the company. |
| `quarter` | body | `number` | yes | Quarter of the year to retrieve earnings info. |
| `year` | body | `number` | yes | Year of the earnings info to retrieve. |
