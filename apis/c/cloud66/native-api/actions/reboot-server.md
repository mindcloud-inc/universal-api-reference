# Reboot Server with Cloud 66

Reboots a server in your Cloud 66 account.

## Endpoint

- **Method:** `POST`
- **Path:** `/stacks/:stack_id/servers/:server_id/reboot`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Reboot Server](https://developers.cloud66.com/v3/endpoints/servers/#reboot-server)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID |
| `server_id` | path | `string` | yes | The server UID |
