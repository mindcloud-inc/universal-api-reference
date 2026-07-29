# Insert Event Log with Rillion Prime Web Service

Write an event log entry in Rillion Prime.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EventLogItem` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. |
| `EventLogItem.Environment` | body | `string` | no | — |
| `EventLogItem.EventType` | body | `string` | no | — |
| `EventLogItem.Source` | body | `string` | no | — |
| `EventLogItem.Task` | body | `string` | no | — |
| `EventLogItem.Message` | body | `string` | no | — |
| `EventLogItem.Description` | body | `string` | no | — |
