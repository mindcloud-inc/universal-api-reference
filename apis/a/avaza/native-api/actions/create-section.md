# Create Section with Avaza

Creates a new section in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Section`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Section](https://api.avaza.com/#!/Section/Section_Post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ProjectIDFK` | body | `number` | no |
| `Title` | body | `string` | no |
| `StartDateUTC` | body | `date` | no |
| `EndDateUTC` | body | `date` | no |
