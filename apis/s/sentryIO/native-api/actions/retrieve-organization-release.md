# Retrieve Organization Release with Sentry IO

Retrieves an organization release from Sentry IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/releases/:version/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [Retrieve Organization Release](https://docs.sentry.io/api/releases/retrieve-an-organizations-release/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
| `version` | path | `string` | yes | The Sentry release version identifier. |
