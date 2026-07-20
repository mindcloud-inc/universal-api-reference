# Create Branded Domain with LinkTwin

Creates a new branded domain in LinkTwin.

## Endpoint

- **Method:** `POST`
- **Path:** `/domain/add`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Create Branded Domain](https://linktw.in/developers#create-a-branded-domain)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `domain` | body | `string` | yes |
| `redirectroot` | body | `string` | no |
| `redirect404` | body | `string` | no |
