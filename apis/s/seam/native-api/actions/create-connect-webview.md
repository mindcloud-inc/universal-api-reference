# Create Connect Webview with Seam

Creates a new connect webview in Seam.

## Endpoint

- **Method:** `POST`
- **Path:** `/connect_webviews/create`
- **Base URL:** `https://connect.getseam.com`
- **Official documentation:** [Create Connect Webview](https://docs.seam.co/latest/api/connect_webviews/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `provider_category` | body | `string` | no | Provider category to show in the Connect Webview. Use `stable` for the broad sandbox-friendly path. |
| `automatically_manage_new_devices` | body | `boolean` | no | Whether newly connected devices should be managed automatically. Seam defaults this to `true`. |
| `wait_for_device_creation` | body | `boolean` | no | Whether the Connect Webview should wait for the first device sync before finishing. Seam defaults this to `false`. |
