# Create Leave Request with Deputy

Creates a new leave request in Deputy.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/resource/Leave`
- **Base URL:** `https://{endpoint}.deputy.com`
- **Official documentation:** [Create Leave Request](https://developer.deputy.com/docs/adding-a-leave-request-for-an-employee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Employee` | body | `number` | yes | The id record number of the employee who is requesting leave. |
| `LeaveRule` | body | `number` | yes | The id record number of the Leave Rule being included. |
| `Company` | body | `number` | yes | The location which the leave application is being applied against. |
| `DateStart` | body | `string` | yes | The start date of the leave in YYYY-MM-DD format. |
| `Start` | body | `number` | yes | The start time of the leave in unix timestamp format. |
| `DateEnd` | body | `string` | yes | The end date of the leave in YYYY-MM-DD format. |
| `End` | body | `number` | yes | The end time of the leave in unix timestamp format. |
| `Comment` | body | `string` | yes | A comment explaining the leave to the manager from the employee. |
