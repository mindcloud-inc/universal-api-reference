# Create Checklist with Checkvist

Creates a checklist in Checkvist.

## Endpoint

- **Method:** `POST`
- **Path:** `/checklists.json`
- **Base URL:** `https://checkvist.com`
- **Official documentation:** [Create Checklist](https://checkvist.com/auth/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checklist.name` | body | `string` | yes | The checklist name. |
| `checklist.public` | body | `boolean` | no | Set to 1 to create a public checklist. |
