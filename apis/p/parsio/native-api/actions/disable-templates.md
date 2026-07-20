# Disable Templates with Parsio

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/disable_many`
- **Base URL:** `https://api.parsio.io`
- **Official documentation:** [Disable Templates](https://help.parsio.io/public-api/parsio-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | Template IDs to disable. |
