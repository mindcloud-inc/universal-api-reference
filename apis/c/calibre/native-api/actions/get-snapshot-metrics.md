# Get Snapshot Metrics with Calibre

Retrieves metrics for a single snapshot from Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Get Snapshot Metrics](https://calibreapp.com/docs/automation/retrieving-metrics#metrics-from-a-single-snapshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.site` | body | `string` | yes | Site slug, found in site settings. |
| `variables.snapshotIid` | body | `number` | yes | Snapshot IID from the snapshot list. |
