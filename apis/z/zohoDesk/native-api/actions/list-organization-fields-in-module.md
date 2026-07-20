# List Organization Fields In Module with Zoho Desk

## Endpoint

- **Method:** `GET`
- **Path:** `/organizationFields`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [List Organization Fields In Module](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Field.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | query | `string` | no | Optional department ID used when fetching module-specific organization fields. |
| `module` | query | `string` | yes | The Zoho Desk module name, such as tickets, contacts, or accounts. |
