# List Tickets with Zoho Desk

List Tickets with optional filters

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [List Tickets](https://github.com/zoho/zohodesk-oas/blob/master/v1.0/Ticket.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter by resolution status of the ticket. You can specify multiple status values here. Send multiple values as a array. |
| `channel` | query | `list<string>` | no | Filter by Channel through which the tickets originated. You can specify multiple channels. Maximum length: 100. Send multiple values as a array. |
| `priority` | query | `string` | no | Filter tickets by Priority. Send multiple values as a array. |
| `receivedInDays` | query | `list<number>` | no | Fetches recent tickets based on `Customer Response Time`. |
| `assignee` | query | `list<string>` | no | Filter tickets by assignee.  Allowed Values: - `Unassiged` - 1 or more valid `assigneeIds` Accepted values: `Unassigned`. Send multiple values as a array. |
| `departmentIds` | query | `list<number>` | no | Select the department(s) from which the tickets need to be queried. Send multiple values as a array. |
| `teamIds` | query | `string` | no | Filter Tickets by Teams.   Allowed Values: - `Unassigned` - 1 or more valid `teamId` Send multiple values as a array. |
| `viewIds` | query | `number` | no | ID of the View to apply while fetching the resources. |
| `include` | query | `list<string>` | no | Specify any additional information you'd like to retrieve related to the tickets. Send multiple values as a array. |
| `fields` | query | `string` | no | Specify fields in your portal that you want to retrieve. (both pre-defined and custom fields are allowed) Send multiple values as a array. |
