# Get Records Modified Since with Quickbase

Retrieves Quickbase records modified after a specified timestamp.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/records/modifiedSince`
- **Base URL:** `https://api.quickbase.com`
- **Official documentation:** [Get Records Modified Since](https://developer.quickbase.com/operation/recordsModifiedSince)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The Quickbase table identifier. |
| `after` | body | `date` | yes | ISO-8601 UTC timestamp to check for changes after. |
| `fieldList[]` | body | `array<number>` | no | Optional field IDs to traverse for dependency-aware change detection. |
| `includeDetails` | body | `boolean` | no | Whether to include the individual record changes in the response. |
