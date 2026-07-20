# List Stories with Storydoc

Retrieves stories from Storydoc.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/stories`
- **Base URL:** `https://api.storydoc.com`
- **Official documentation:** [List Stories](https://docs.storydoc.com/operation/operation-getstories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list<string>` | no | Filter stories by status. Accepted values: `Archived`, `Draft`, `Live`. |
