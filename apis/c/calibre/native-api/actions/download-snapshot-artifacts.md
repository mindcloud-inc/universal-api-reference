# Download Snapshot Artifacts with Calibre

Retrieves artifact download URLs for a snapshot from Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Download Snapshot Artifacts](https://calibreapp.com/docs/automation/snapshots#download-snapshot-artifacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.site` | body | `string` | yes | Site slug, found in site settings. |
| `variables.snapshotIid` | body | `number` | yes | Snapshot IID used by the documented snapshot APIs. |
| `variables.artifactName` | body | `string` | no | Snapshot test artifact enum value. |
| `variables.mediaName` | body | `string` | no | Snapshot media enum value. |
