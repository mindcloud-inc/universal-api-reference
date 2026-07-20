# Analyze IP with Opportify

Analyzes an IP address in Opportify for risk and geolocation.

## Endpoint

- **Method:** `POST`
- **Path:** `/ip/analyze`
- **Base URL:** `https://api.opportify.ai/insights/v1`
- **Official documentation:** [Analyze IP](https://www.opportify.ai/docs/api/api-reference/analyze-ip)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | body | `string` | yes | The IPv4 or IPv6 address to analyze. |
| `enableAI` | body | `boolean` | no | Enable AI-driven analysis for the IP address. Default is `false`. |
