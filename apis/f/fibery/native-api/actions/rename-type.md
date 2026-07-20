# Rename Type with Fibery

Updates an existing type in Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/commands`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Rename Type](https://the.fibery.io/@public/User_Guide/Guide/Type-API-262)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromName` | body | `string` | yes | Existing Fibery type name to rename. |
| `toName` | body | `string` | yes | New Fibery type name. |
