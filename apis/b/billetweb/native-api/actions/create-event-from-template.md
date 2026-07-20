# Create Event From Template with Billetweb

Creates a new event in Billetweb from a template.

## Endpoint

- **Method:** `POST`
- **Path:** `/event/:id/clone`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [Create Event From Template](https://www.billetweb.fr/bo/api.php#/api/event/:id/clone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Source template event identifier. |
| `name` | body | `string` | yes | Name of the new event. |
| `place` | body | `string` | no | Location of the new event. |
| `start` | body | `number` | no | Event start time as a Unix timestamp. |
| `end` | body | `number` | no | Event end time as a Unix timestamp. |
| `clone_dates` | body | `boolean` | no | Whether to duplicate the template event sessions. |
| `clone_lists` | body | `boolean` | no | Whether to duplicate related list operations from the template event. |
| `clone_seating` | body | `boolean` | no | Whether to duplicate numbered seating from the template event. |
