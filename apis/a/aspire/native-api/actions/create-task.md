# Create Task with Aspire

Creates a new task in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `Tasks`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Task](https://guide.youraspire.com/apidocs/tasks-6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AssignedTo` | body | `list<string>` | yes | Contacts responsible for completing the milestone Send multiple values as a array. |
| `Subject` | body | `string` | yes | Summary or title of task |
| `Notes` | body | `string` | no | — |
| `OpportunityID` | body | `list<number>` | no | — |
| `Priority` | body | `string` | no | — |
| `PropertyID` | body | `number` | no | — |
| `DueDate` | body | `string` | no | — |
| `StartDate` | body | `string` | no | — |
| `WorkTicketID` | body | `number` | no | Unique identifier for work ticket |
