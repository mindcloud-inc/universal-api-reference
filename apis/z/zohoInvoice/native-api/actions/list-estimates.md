# List Estimates with Zoho Invoice

Retrieves estimates from Zoho Invoice.

## Endpoint

- **Method:** `GET`
- **Path:** `/estimates`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [List Estimates](https://www.zoho.com/invoice/api/v3/estimates/#list-estimates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `zcrm_potential_id` | query | `number` | no | Potential ID of a Deal in CRM. |
