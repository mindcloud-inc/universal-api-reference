# Rebuild Catalog PDF with Catalog Machine

Starts a catalog PDF rebuild job in Catalog Machine.

## Endpoint

- **Method:** `GET`
- **Path:** `/catalogs/:permalink/rebuild`
- **Base URL:** `https://www.catalogmachine.com/api/v1`
- **Official documentation:** [Rebuild Catalog PDF](https://help.catalogmachine.com/en/articles/3667421-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `permalink` | path | `string` | yes | Catalog permalink identifier. |
