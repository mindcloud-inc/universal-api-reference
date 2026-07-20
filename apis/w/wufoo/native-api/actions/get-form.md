# Get Form with Wufoo

Retrieves a form from Wufoo by identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:identifier.json`
- **Base URL:** `https://{subdomain}.wufoo.com/api/v3`
- **Official documentation:** [Get Form](https://wufoo.github.io/docs/#forms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The Wufoo form hash or URL slug, for example `z18tlglo01kf7h1`. |
