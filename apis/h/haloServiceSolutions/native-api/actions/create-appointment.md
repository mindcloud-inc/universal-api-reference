# Create Appointment with Halo Service Solutions

Creates a new appointment in Halo Service Solutions.

## Endpoint

- **Method:** `POST`
- **Path:** `/Appointment`
- **Base URL:** `https://mindcloud.halopsa.com/api`
- **Official documentation:** [Create Appointment](https://usehalo.com/swagger/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ticket_id` | body | `number` | no |
| `agent_id` | body | `number` | yes |
| `start_date` | body | `date` | yes |
| `end_date` | body | `date` | yes |
