# Get Release Metadata with PyPI

Retrieves release metadata, ownership, and vulnerabilities from PyPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/pypi/:project/:version/json`
- **Base URL:** `https://pypi.org`
- **Official documentation:** [Get Release Metadata](https://docs.pypi.org/api/json/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | path | `string` | yes | The normalized PyPI project name to inspect. |
| `version` | path | `string` | yes | The release version string to inspect. |
