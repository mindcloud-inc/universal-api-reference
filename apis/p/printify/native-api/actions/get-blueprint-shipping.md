# Get Blueprint Shipping with Printify

Retrieves blueprint shipping details from Printify.

## Endpoint

- **Method:** `GET`
- **Path:** `/catalog/blueprints/:blueprint_id/print_providers/:print_provider_id/shipping.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Get Blueprint Shipping](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_id` | path | `number` | yes | Printify blueprint id. |
| `print_provider_id` | path | `number` | yes | Printify print provider id. |
