# Import Templates with Bannerbear

Imports templates into Bannerbear.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/templates/import`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [Import Templates](https://developers.bannerbear.com/v2/#import-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publications[]` | body | `array<string>` | yes | An array of public library Publication IDs to import. |
