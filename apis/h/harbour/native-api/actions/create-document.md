# Create Document with Harbour

Creates a new document in Harbour.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://api.myharbourshare.com/v2`
- **Official documentation:** [Create Document](https://developers.harbourshare.com/v2#create-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the document. |
| `files[]` | body | `array<object>` | yes | Initial file metadata array. Each entry should include at least name and type. |
| `created_by` | body | `string` | no | Optional Harbour user identifier to attribute document creation. |
| `state` | body | `string` | no | Optional initial document state. Harbour defaults to draft. |
