# Create Work Ticket Time with Aspire

Creates a new work ticket time in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `WorkTicketTimes`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Work Ticket Time](https://cloud-api.youraspire.com/swagger/index.html#/WorkTicketTimes/WorkTicketTimes_Create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ContactID` | body | `number` | no |
| `WorkTicketID` | body | `number` | no |
| `StartTime` | body | `date` | yes |
| `StartLatitude` | body | `number` | no |
| `StartLongitude` | body | `number` | no |
| `RouteID` | body | `number` | no |
| `CrewLeaderContactID` | body | `number` | no |
| `EndTime` | body | `date` | yes |
| `EndLatitude` | body | `number` | no |
| `EndLongitude` | body | `number` | no |
