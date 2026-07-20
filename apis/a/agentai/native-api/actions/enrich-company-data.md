# Enrich Company Data with Agent.ai

Retrieves enriched company data from Agent.ai by domain.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/get_company_object`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Enrich Company Data](https://docs.agent.ai/api-reference/get-data/enrich-company-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Company domain to enrich. |
