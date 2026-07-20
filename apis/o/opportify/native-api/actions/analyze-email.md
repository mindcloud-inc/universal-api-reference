# Analyze Email with Opportify

Analyzes an email address in Opportify for deliverability and risk.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/analyze`
- **Base URL:** `https://api.opportify.ai/insights/v1`
- **Official documentation:** [Analyze Email](https://www.opportify.ai/docs/api/api-reference/analyze-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address to validate. |
| `enableAI` | body | `boolean` | no | Enable AI-driven risk analysis. Optional; defaults to `true`. |
| `enableAutoCorrection` | body | `boolean` | no | Controls email auto-correction behavior. Default: `false`.  - When set to `true`: If the system is highly confident about a correction, it will automatically apply it. The analysis will be performed on the corrected email address. The response will include the corrected email in `emailAddress` and `emailCorrection`, with the original input preserved in `emailAutoCorrectedFrom`. - When set to `false`: The system will still identify and return potential corrections in the `emailCorrection` field when confident, but the analysis will remain based on the original email address provided in the input. The `emailAutoCorrectedFrom` field will not be present. |
| `enableDomainEnrichment` | body | `boolean` | no | Include domain-level enrichment details. Optional; defaults to `true`. Set to `false` to omit the `domain` block even when the data exists. |
