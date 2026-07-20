# Add New Contact To Automation with GetSales.io

## Endpoint

- **Method:** `POST`
- **Path:** `/flows/api/flows/{flowUuid}/add-new-lead`
- **Base URL:** `https://amazing.getsales.io`
- **Official documentation:** [Add New Contact To Automation](https://api.getsales.io/api/openapi/automations/addnewleadtoflow.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowUuid` | path | `string` | yes | UUID of the automation to add the new contact to. |
| `lead.linkedin_id` | body | `string` | yes | Contact LinkedIn ID or profile handle. |
| `lead.first_name` | body | `string` | no | Contact first name. |
| `lead.last_name` | body | `string` | no | Contact last name. |
| `lead.company_name` | body | `string` | no | Contact company name. |
| `lead.email` | body | `string` | no | Contactable email address for the contact. |
| `list_uuid` | body | `string` | yes | UUID of the target list. |
| `flow_segment_id` | body | `number` | no | ID of a specific automation segment. Defaults to 1 when omitted. |
| `skip_if_lead_exists` | body | `boolean` | no | When true, existing contacts are not added to the automation. |
