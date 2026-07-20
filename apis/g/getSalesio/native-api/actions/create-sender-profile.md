# Create Sender Profile with GetSales.io

## Endpoint

- **Method:** `POST`
- **Path:** `/flows/api/sender-profiles`
- **Base URL:** `https://amazing.getsales.io`
- **Official documentation:** [Create Sender Profile](https://api.getsales.io/api/openapi/sender-profiles/createsenderprofile.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignee_user_id` | body | `number` | no | ID of the user assigned to the sender profile. |
| `first_name` | body | `string` | no | Sender first name. |
| `last_name` | body | `string` | no | Sender last name. |
| `label` | body | `string` | no | Custom sender profile label. |
