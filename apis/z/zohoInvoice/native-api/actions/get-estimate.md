# Get Estimate with Zoho Invoice

Retrieves an estimate from Zoho Invoice.

## Endpoint

- **Method:** `GET`
- **Path:** `/estimates/:estimate_id`
- **Base URL:** `https://www.zohoapis.com/invoice/v3`
- **Official documentation:** [Get Estimate](https://www.zoho.com/invoice/api/v3/estimates/#get-an-estimate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `estimate_id` | path | `string` | yes | Unique identifier of the estimate. |
| `accept` | query | `string` | no | Get the estimate as json, pdf, or html. Accepted values: `0`, `1`, `2`. |
| `print` | query | `boolean` | no | Print the exported PDF. |
