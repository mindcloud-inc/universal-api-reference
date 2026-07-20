# Create Employee with Deputy

Creates a new employee in Deputy.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/management/v2/employees`
- **Base URL:** `https://{endpoint}.deputy.com`
- **Official documentation:** [Create Employee](https://developer.deputy.com/docs/adding-an-employee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | Employee payload object. |
| `firstName` | body | `string` | yes | The employee's given name. |
| `lastName` | body | `string` | yes | The employee's family name. |
| `displayName` | body | `string` | yes | The employee's display name. |
| `primaryLocation` | body | `object` | no | The employee's primary location object. |
| `id` | body | `number` | no | The id of the employee's primary location. |
| `startDate` | body | `date` | no | The employee's start date. |
| `position` | body | `string` | no | The employee's position title. |
| `contact` | body | `object` | no | Employee contact object. |
| `email1` | body | `string` | no | Primary work email address. |
| `phone1` | body | `string` | no | Primary phone number. |
| `externalId` | body | `string` | no | An external identifier for the employee. |
