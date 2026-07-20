# Create Schema with Rossum

Creates a new schema in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/schemas`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Create Schema](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the schema to create. |
| `content` | body | `list<object>` | yes | Schema content array describing the Rossum sections and datapoints. |
