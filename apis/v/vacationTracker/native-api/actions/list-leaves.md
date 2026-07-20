# List Leaves with Vacation Tracker

## Endpoint

- **Method:** `GET`
- **Path:** `/leaves`
- **Base URL:** `https://api.vacationtracker.io/v1`
- **Official documentation:** [List Leaves](https://vacationtracker.io/developers/api/leaves/listLeaves)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `string` | yes | Date in YYYY-MM-DD format. |
| `endDate` | query | `string` | yes | Date in YYYY-MM-DD format. Cannot be before the start date. |
| `status` | query | `list<string>` | no | Leave request status. Defaults to APPROVED. Accepted values: `APPROVED`, `CANCELLED`, `DELETED`, `DENIED`, `EXPIRED`, `OPEN`. |
| `expand` | query | `list<string>` | no | Related leave request object to expand. Accepted values: `approver`, `leaveType`, `user`. |
