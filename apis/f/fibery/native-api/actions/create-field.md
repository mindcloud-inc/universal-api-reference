# Create Field with Fibery

Creates a new field in Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/commands`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Create Field](https://the.fibery.io/@public/User_Guide/Guide/Field-API-263)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `holderType` | body | `string` | yes | Type that will receive the new field. |
| `name` | body | `string` | yes | New field name including the namespace prefix. |
| `fieldType` | body | `string` | yes | Fibery field type, for example `fibery/text`. |
| `meta` | body | `object` | no | Optional Fibery field meta object. |
