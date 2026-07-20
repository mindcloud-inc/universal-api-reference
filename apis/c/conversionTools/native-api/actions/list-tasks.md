# List Tasks with Conversion Tools

Retrieves up to 50 recent conversion tasks from Conversion Tools.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://api.conversiontools.io/v1`
- **Official documentation:** [List Tasks](https://api.conversiontools.io/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list<string>` | no | Optional provider status to filter the returned tasks. Accepted values: `ERROR`, `PENDING`, `RUNNING`, `SUCCESS`. |
