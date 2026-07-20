# List Unattended Groups with Zoho Assist

Lists existing unattended computer groups in Zoho Assist.

## Endpoint

- **Method:** `GET`
- **Path:** `/unattended_computer/group`
- **Base URL:** `https://assist.zoho.com/api/v2`
- **Official documentation:** [List Unattended Groups](https://www.zoho.com/assist/api/getunattendedgroup.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `department_id` | query | `string` | yes | Department in which the group exists. |
| `q` | query | `string` | no | Optional name filter for groups. |
