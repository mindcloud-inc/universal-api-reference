# Get Multiple Products with ShipBob

## Endpoint

- **Method:** `GET`
- **Path:** `1.0/product`
- **Base URL:** `https://{apiSubdomain}.shipbob.com/`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Search` | query | `string` | no | — |
| `ReferenceIds` | query | `array<string>` | no | list of reference IDs to filter by |
