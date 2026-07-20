# List Snapshots with HiDrive

Retrieves snapshots from HiDrive.

## Endpoint

- **Method:** `GET`
- **Path:** `/snapshot`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [List Snapshots](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/snapshot_GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | query | `string` | no | Path to list snapshots for. |
| `pid` | query | `string` | no | Object public ID to list snapshots for. |
| `scope` | query | `string` | no | Snapshot scope, defaults to user. |
