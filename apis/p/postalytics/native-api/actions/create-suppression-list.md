# Create Suppression List with Postalytics

Creates a suppression list in Postalytics.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/lists/suppression`
- **Base URL:** `https://api.postalytics.com`
- **Official documentation:** [Create Suppression List](https://docs.postalytics.com/references/postalytics-rest-api/create-suppression-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Country` | body | `string` | no | Country code for the list. |
| `Name` | body | `string` | no | Suppression list name. |
