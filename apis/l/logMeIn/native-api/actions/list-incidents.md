# List Incidents with LogMeIn

Retrieves a list of incidents from LogMeIn.

## Endpoint

- **Method:** `GET`
- **Path:** `/goto-resolve-ticketing/v1/incidents`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [List Incidents](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceId` | query | `string` | no | Service identifier. Leave blank for all services. |
| `keyword` | query | `string` | no | String to filter incidents. |
| `pageSize` | query | `number` | no | Number of incidents per page. |
| `pageNumber` | query | `number` | no | Page number to retrieve. |
| `sort` | query | `string` | no | Field to sort by. Prefix with '-' for descending order. |
| `assignedTo` | query | `string` | no | Assigned user IDs as a comma-separated list or repeated query parameter. |
| `requestedBy` | query | `string` | no | Requested-by user IDs as a comma-separated list or repeated query parameter. |
| `ticketType` | query | `string` | no | Ticket type filter. |
| `category` | query | `string` | no | Category names as a comma-separated list or repeated query parameter. |
| `priority` | query | `string` | no | Priority values as a comma-separated list or repeated query parameter. |
| `status` | query | `string` | no | Status names as a comma-separated list or repeated query parameter. |
| `tag` | query | `string` | no | Tag names as a comma-separated list or repeated query parameter. |
| `createdAtFrom` | query | `date` | no | Filter incidents created from this date. |
| `createdAtTo` | query | `date` | no | Filter incidents created until this date. |
| `dueDateFrom` | query | `date` | no | Filter incidents due from this date. |
| `dueDateTo` | query | `date` | no | Filter incidents due until this date. |
| `updatedAtFrom` | query | `date` | no | Filter incidents updated from this date. |
| `updatedAtTo` | query | `date` | no | Filter incidents updated until this date. |
| `include` | query | `string` | no | Related entities to include as a comma-separated list or repeated query parameter. |
| `extraFields` | query | `string` | no | Extra fields to include as a comma-separated list or repeated query parameter. |
