# List Blueprint Variants with Printify

Retrieves blueprint variants from Printify.

## Endpoint

- **Method:** `GET`
- **Path:** `/catalog/blueprints/:blueprint_id/print_providers/:print_provider_id/variants.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [List Blueprint Variants](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_id` | path | `number` | yes | Printify blueprint id. |
| `print_provider_id` | path | `number` | yes | Printify print provider id. |
