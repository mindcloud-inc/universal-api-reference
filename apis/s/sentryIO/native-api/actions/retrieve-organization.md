# Retrieve Organization with Sentry IO

Retrieves an organization from Sentry IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_id_or_slug/`
- **Base URL:** `https://sentry.io/api/0`
- **Official documentation:** [Retrieve Organization](https://docs.sentry.io/api/organizations/retrieve-an-organization/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id_or_slug` | path | `string` | yes | The Sentry organization ID or slug. |
