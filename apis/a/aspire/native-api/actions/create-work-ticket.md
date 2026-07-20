# Create As Needed Work Tickets with Aspire

## Endpoint

- **Method:** `POST`
- **Path:** `WorkTickets/CreateAsNeededWorkTickets`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create As Needed Work Tickets](https://guide.youraspire.com/apidocs/workticketscreateasneededworktickets-1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `EndDateTime` | body | `string` | no |
| `RouteId` | body | `list<string>` | yes |
| `ScheduledStartDate` | body | `string` | yes |
| `StartDateTime` | body | `string` | no |
| `OpportunityServiceId` | body | `list` | yes |
| `HoursPerDay` | body | `string` | no |
