# Create Snapshot with Daytona

Creates a new snapshot in Daytona.

## Endpoint

- **Method:** `POST`
- **Path:** `/snapshots`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [Create Snapshot](https://www.daytona.io/docs/tools/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the snapshot. |
| `imageName` | body | `string` | no | The image name of the snapshot. |
| `entrypoint[]` | body | `array<string>` | no | Entrypoint command for the snapshot. |
| `cpu` | body | `number` | no | CPU cores allocated to the resulting sandbox. |
| `gpu` | body | `number` | no | GPU units allocated to the resulting sandbox. |
| `memory` | body | `number` | no | Memory allocated to the resulting sandbox in GB. |
| `disk` | body | `number` | no | Disk space allocated to the sandbox in GB. |
| `buildInfo` | body | `object` | no | Build information for the snapshot. |
| `regionId` | body | `string` | no | ID of the region where the snapshot will be available. |
