# Create Agreement with Harbour

Creates a new agreement in Harbour.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.harbourshare.com/v1/agreements`
- **Base URL:** `https://api.myharbourshare.com/v2`
- **Official documentation:** [Create Agreement](https://developers.harbourshare.com/#create-agreement)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_upload` | body | `object` | yes | Object with name and base64 for the agreement file. |
| `agreement_data` | body | `object` | yes | Agreement metadata, inputs, and template settings. |
