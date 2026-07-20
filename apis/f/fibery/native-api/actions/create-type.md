# Create Type with Fibery

Creates a new type in Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/commands`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Create Type](https://the.fibery.io/@public/User_Guide/Guide/Type-API-262)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | New Fibery type name, for example `Project Tracking/My Type`. |
| `color` | body | `string` | no | Optional UI color hex for the type. |
| `secured` | body | `boolean` | no | Whether the type is secured. |
