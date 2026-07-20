# Create Task with Agile CRM

Creates a new task in Agile CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://mindcloud.agilecrm.com/dev/api`
- **Official documentation:** [Create Task](https://github.com/agilecrm/rest-api#54-create-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | yes | — |
| `type` | body | `list<string>` | yes | Accepted values: `CALL`, `EMAIL`, `FOLLOW_UP`, `MEETING`, `MILESTONE`, `OTHER`, `SEND`, `TWEET`. |
| `priority_type` | body | `list<string>` | yes | Accepted values: `HIGH`, `LOW`, `NORMAL`. |
| `due` | body | `date` | yes | — |
