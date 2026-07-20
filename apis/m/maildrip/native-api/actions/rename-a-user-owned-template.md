# Rename a user-owned template with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/templates/my-templates/{templateId}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Rename a user-owned template](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | ID of the template to update |
| `name` | body | `string` | no | New name for the template |
