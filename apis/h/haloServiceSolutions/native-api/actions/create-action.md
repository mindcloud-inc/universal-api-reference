# Create Action with Halo Service Solutions

Creates a new action in Halo Service Solutions.

## Endpoint

- **Method:** `POST`
- **Path:** `/Actions`
- **Base URL:** `https://mindcloud.halopsa.com/api`
- **Official documentation:** [Create Action](https://usehalo.com/swagger/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ticket_id` | body | `number` | yes |
| `outcome` | body | `string` | yes |
| `note` | body | `string` | no |
