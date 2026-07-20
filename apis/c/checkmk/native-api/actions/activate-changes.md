# Activate Changes with Checkmk

Starts a pending changes activation run in Checkmk.

## Endpoint

- **Method:** `POST`
- **Path:** `/domain-types/activation_run/actions/activate-changes/invoke`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Activate Changes](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sites[]` | body | `array<string>` | no | Site IDs to activate. Omit to use all sites. |
| `redirect` | body | `boolean` | no | Whether Checkmk should redirect while activation proceeds. |
