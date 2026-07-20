# Insert/Update Record(s) with Quickbase

Creates Quickbase records, or updates matching records if they exist.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/records`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Insert/Update Record(s)](https://developer.quickbase.com/operation/upsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | The Quickbase table identifier that will receive the record changes. |
| `data` | body | `string<string>` | yes | JSON string containing the Quickbase record array payload, for example [{"6":{"value":"Acme"}}]. |
