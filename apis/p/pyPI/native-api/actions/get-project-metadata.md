# Get Project Metadata with PyPI

Retrieves project metadata and release history from PyPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/pypi/:project/json`
- **Base URL:** `https://pypi.org`
- **Official documentation:** [Get Project Metadata](https://docs.pypi.org/api/json/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | The normalized PyPI project name to inspect. |
