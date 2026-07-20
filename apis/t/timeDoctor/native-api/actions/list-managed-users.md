# List Managed Users with Time Doctor

Retrieves managed users from Time Doctor.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/1.0/users/:userId/managed`
- **Base URL:** `https://api2.timedoctor.com`
- **Official documentation:** [List Managed Users](https://api2.timedoctor.com/#operation/getManagedUsers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | ID of the manager or user to inspect. Use `me` for the caller. |
