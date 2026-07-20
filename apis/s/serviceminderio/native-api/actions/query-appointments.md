# Query Appointments with serviceminder.io

Finds appointments in ServiceMinder by date, contact, or agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/appointments/query`
- **Base URL:** `https://serviceminder.com/api`
- **Official documentation:** [Query Appointments](https://serviceminder.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FromDate` | body | `date` | no | Start date for appointment query. |
| `ThroughDate` | body | `date` | no | End date for appointment query. |
| `ContactId` | body | `number` | no | Filter by contact identifier. |
| `ServiceAgentId` | body | `number` | no | Filter by service agent identifier. |
