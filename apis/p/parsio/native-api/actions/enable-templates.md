# Enable Templates with Parsio

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/enable_many`
- **Base URL:** `https://api.parsio.io`
- **Official documentation:** [Enable Templates](https://help.parsio.io/public-api/parsio-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | Template IDs to enable. |
