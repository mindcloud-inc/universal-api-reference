# Manifest Orders (Shipments) with Starshipit

## Endpoint

- **Method:** `POST`
- **Path:** `/manifests/shipments`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Manifest Orders (Shipments)](https://api-docs.starshipit.com/#adc9e882-abfd-4488-b0c9-c1119591bdd6)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tracking_numbers[]` | body | `array<string>` | no |
| `use_order_numbers` | body | `boolean` | no |
