# Save Layer with MOBIDI

Creates or updates a layer in MOBIDI.

## Endpoint

- **Method:** `POST`
- **Path:** `/MobidiWorkspaceManagerHandler`
- **Base URL:** `https://servis2.dece.com.tr`
- **Official documentation:** [Save Layer](https://servis2.dece.com.tr/mobidiworkspacemanagerhandler?op=.wsdl&loginWithGuest=1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Layer` | body | `string` | yes | Serialized MobidiLayer payload. |
| `IsNewLayer` | body | `boolean` | no | Whether the layer is new. |
| `LayerIdControl` | body | `boolean` | no | Whether to enforce layer ID control. |
