# Delete Field with Fibery

Deletes an existing field from Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/commands`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Delete Field](https://the.fibery.io/@public/User_Guide/Guide/Field-API-263)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `holderType` | body | `string` | yes | Type that owns the field. |
| `name` | body | `string` | yes | Field name to delete. |
| `deleteValues` | body | `boolean` | no | Delete existing field values before removing the field. |
