# List Blueprint Print Providers with Printify

Retrieves blueprint print providers from Printify.

## Endpoint

- **Method:** `GET`
- **Path:** `/catalog/blueprints/:blueprint_id/print_providers.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [List Blueprint Print Providers](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_id` | path | `number` | yes | Printify blueprint id. |
