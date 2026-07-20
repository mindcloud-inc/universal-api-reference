# Get Time Entry Entities with Beebole

Retrieves available entities for a time entry in Beebole.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://beebole-apps.com/api/v2`
- **Official documentation:** [Get Time Entry Entities](https://beebole.com/help/api#examples-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company.id` | body | `number` | no | Provide a Beebole company ID to list its available projects for time entry creation. |
| `project.id` | body | `number` | no | Provide a Beebole project ID to list its available subprojects for time entry creation. |
| `date` | body | `string` | yes | The date used by Beebole to evaluate which entities are available. |
