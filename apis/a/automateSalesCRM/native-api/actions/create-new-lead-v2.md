# Create New Lead V2 with Automate Sales CRM

Creates a new lead in Automate Sales CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `ab-crm-webhook`
- **Base URL:** `https://api.automatebusiness.com/functions/v1/`
- **Official documentation:** [Create New Lead V2](https://support.automatebusiness.com/en/article/how-to-integrate-lead-forms-with-automated-crm-app-through-pabbly-ckva8e/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Lead or contact name sent to the public lead webhook. |
| `email` | body | `string` | no | Lead email address. |
| `phone` | body | `string` | no | Lead phone number. |
| `lead_title` | body | `string` | no | Lead title from the provider's lead-creation UI. |
| `source` | body | `string` | no | Lead source label. |
| `pipeline` | body | `string` | no | Optional pipeline label when workspace defaults are not sufficient. |
| `stage` | body | `string` | no | Optional stage label when workspace defaults are not sufficient. |
| `sales_person` | body | `string` | no | Optional sales person or assignee label from the provider UI. |
