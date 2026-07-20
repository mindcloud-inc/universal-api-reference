# Create Issue with Ninety.io

Creates a new issue in Ninety.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/issues`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Create Issue](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | — |
| `teamId` | body | `string` | yes | — |
| `interval` | body | `string` | no | Issue classification |
| `description` | body | `string` | no | HTML description of the Issue |
| `priority` | body | `number` | no | Priority level from 0 (none) to 5 (highest) |
