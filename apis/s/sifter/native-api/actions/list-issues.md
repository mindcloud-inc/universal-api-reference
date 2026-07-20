# List Issues with Sifter

Retrieves issues for a project from Sifter.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/issues`
- **Base URL:** `https://{subdomain}.sifterapp.com/api`
- **Official documentation:** [List Issues](https://sifterapp.com/developer/documentation/issues/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `a` | query | `string` | no | — |
| `c` | query | `string` | no | — |
| `m` | query | `string` | no | — |
| `p` | query | `string` | no | One or more priority IDs separated by hyphens, for example 1-2. |
| `project_id` | path | `number` | yes | The Sifter project ID. |
| `q` | query | `string` | no | Search issue text. |
| `s` | query | `string` | no | One or more status IDs separated by hyphens, for example 209607-209608. |
