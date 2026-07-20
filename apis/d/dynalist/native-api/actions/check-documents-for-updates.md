# Check Documents For Updates with Dynalist

Checks Dynalist documents for updates.

## Endpoint

- **Method:** `POST`
- **Path:** `/doc/check_for_updates`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Check Documents For Updates](https://apidocs.dynalist.io/#check-if-documents-has-been-updated)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_ids[]` | body | `array<string>` | yes | IDs of the documents to check for latest version numbers. |
