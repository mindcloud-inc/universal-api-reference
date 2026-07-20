# Create Service Agreement with Previsto

Creates a new service agreement in Previsto.

## Endpoint

- **Method:** `POST`
- **Path:** `/agreements`
- **Base URL:** `https://api.previsto.io`
- **Official documentation:** [Create Service Agreement](https://developer.previsto.com/service-agreements/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | yes | Service agreement description. |
| `contactId` | body | `string` | yes | Previsto contact ID. |
