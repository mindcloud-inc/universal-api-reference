# List Nodes By Type with ACLU

Retrieves Torture Database nodes by content type.

## Endpoint

- **Method:** `GET`
- **Path:** `/getnode/retrieve.json`
- **Base URL:** `https://www.thetorturedatabase.org/rest`
- **Official documentation:** [List Nodes By Type](https://www.thetorturedatabase.org/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Zero-based page number. The docs say page=0 by default. |
| `name` | query | `string` | yes | Use one documented value exactly: agency, Authors/Recipients, Document Types, Techniques, detainee, document, incident, location, official, or source. |
