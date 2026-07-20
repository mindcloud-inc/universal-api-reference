# Delete Type with Fibery

Deletes an existing type from Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/commands`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Delete Type](https://the.fibery.io/@public/User_Guide/Guide/Type-API-262)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Fibery type name to delete. |
| `deleteEntities` | body | `boolean` | no | Delete entities stored in the type before removing the type. |
| `deleteRelatedFields` | body | `boolean` | no | Delete related fields on other types. |
