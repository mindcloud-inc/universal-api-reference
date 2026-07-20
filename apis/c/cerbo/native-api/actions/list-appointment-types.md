# List Appointment Types with Cerbo

Retrieves appointment types from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/appointment_types`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Appointment Types](https://docs.cer.bo/#tag/Appointment-Types/operation/listAppointmentTypes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_deleted` | query | `string` | no | If specified and not empty, results will include deleted appointment types. Any non-empty value is treated as true. |
