# Generate Client Framework Install Instructions with Appzi

Generates client framework install snippets for Appzi.

## Endpoint

- **Method:** `GET`
- **Path:** `https://docs.appzi.io/installation/`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Generate Client Framework Install Instructions](https://docs.appzi.io/installation/#client-side-frameworks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | query | `string` | yes | Portal token inserted into the generated framework install snippet. |
| `framework` | query | `string` | yes | Client framework documented by Appzi: react, vue, or angular. |
