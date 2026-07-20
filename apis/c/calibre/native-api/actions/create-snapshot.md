# Create Snapshot with Calibre

Creates a new snapshot for a site in Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Create Snapshot](https://calibreapp.com/docs/automation/snapshots#create-a-snapshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.site` | body | `string` | yes | Site slug, found in site settings. |
| `variables.ref` | body | `string` | no | Reference label for this snapshot, such as a commit SHA or branch name. |
| `variables.client` | body | `string` | no | Client name that created the snapshot. |
