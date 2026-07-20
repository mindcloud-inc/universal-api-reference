# Run Sync Now with Files.com

Manually runs a sync in Files.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/syncs/:id/manual_run`
- **Base URL:** `{siteUrl}/api/rest/v1`
- **Official documentation:** [Run Sync Now](https://developers.files.com/rest/resources/integrations/syncs#manually-run-sync)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric sync ID to run. |
