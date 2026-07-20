# Batch Analyze IPs with Opportify

Creates an asynchronous IP analysis job in Opportify.

## Endpoint

- **Method:** `POST`
- **Path:** `/ip/batch`
- **Base URL:** `https://api.opportify.ai/insights/v1`
- **Official documentation:** [Batch Analyze IPs](https://www.opportify.ai/docs/api/api-reference/batch-analyze-ips)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ips[]` | body | `array<string>` | yes | Array of IP addresses to analyze. |
| `name` | body | `string` | no | Optional name for the batch job. |
| `enableAI` | body | `boolean` | no | Enable AI-based analysis for insights. |
