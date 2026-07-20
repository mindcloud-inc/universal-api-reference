# Cancel Build Tasks For Datamodel with Sisense

Cancels build tasks for a Sisense datamodel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/builds`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Cancel Build Tasks For Datamodel](https://developer.sisense.com/guides/restApi/datamodels.v2.html#api-structure)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datamodelId` | body | `string` | no | The datamodel oid whose build tasks should be cancelled. |
