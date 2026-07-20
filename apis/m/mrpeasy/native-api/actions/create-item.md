# Create Item with MRPeasy

Creates a new stock item in MRPeasy.

## Endpoint

- **Method:** `POST`
- **Path:** `/items`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Create Item](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | Item code. |
| `title` | body | `string` | yes | Item title. |
