# Create Deal with Paycove

Creates a deal in Paycove.

## Endpoint

- **Method:** `POST`
- **Path:** `deals/with-relations`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Create Deal](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | body | `object` | yes | Contact object. Provide an existing id or name and email to create a new contact. |
| `crm_deal_id` | body | `string` | no | Associated CRM deal id. |
| `line_items[]` | body | `array<object>` | yes | Array of line item objects. |
| `name` | body | `string` | yes | Name of the deal. |
| `org` | body | `object` | yes | Organization object. Provide an existing id or organization fields. |
| `type` | body | `string` | yes | Deal type. Allowed values: invoice or quote. |
