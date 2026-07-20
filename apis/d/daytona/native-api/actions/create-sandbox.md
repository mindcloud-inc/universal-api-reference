# Create Sandbox with Daytona

Creates a new sandbox in Daytona.

## Endpoint

- **Method:** `POST`
- **Path:** `/sandbox`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [Create Sandbox](https://www.daytona.io/docs/tools/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The name of the sandbox. |
| `snapshot` | body | `string` | no | The ID or name of the snapshot used for the sandbox. |
| `user` | body | `string` | no | User associated with the sandbox. |
| `target` | body | `string` | no | Target region where the sandbox will be created. |
| `class` | body | `string` | no | Sandbox class type. |
| `public` | body | `boolean` | no | Whether the sandbox HTTP preview is publicly accessible. |
| `env` | body | `object` | no | Environment variables for the sandbox. |
| `labels` | body | `object` | no | Labels for the sandbox. |
| `networkBlockAll` | body | `boolean` | no | Whether to block all network access for the sandbox. |
| `networkAllowList` | body | `string` | no | Comma-separated list of allowed CIDR network addresses. |
| `cpu` | body | `number` | no | CPU cores allocated to the sandbox. |
| `gpu` | body | `number` | no | GPU units allocated to the sandbox. |
| `memory` | body | `number` | no | Memory allocated to the sandbox in GB. |
| `disk` | body | `number` | no | Disk space allocated to the sandbox in GB. |
| `autoStopInterval` | body | `number` | no | Auto-stop interval in minutes. |
| `autoArchiveInterval` | body | `number` | no | Auto-archive interval in minutes. |
| `autoDeleteInterval` | body | `number` | no | Auto-delete interval in minutes. |
| `volumes[]` | body | `array<object>` | no | Volumes to attach to the sandbox. |
| `buildInfo` | body | `object` | no | Build information for the sandbox. |
