# Get Packaging with ReadyCloud Suite

Retrieves a packaging record from ReadyCloud Suite.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orgs/:orgPk/packaging/:packagingPk/`
- **Base URL:** `https://www.readycloud.com`
- **Official documentation:** [Get Packaging](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-09-packaging.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgPk` | path | `string` | yes | ReadyCloud organization identifier. |
| `packagingPk` | path | `string` | yes | ReadyCloud packaging identifier. |
