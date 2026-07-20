# Publish Live Datamodel with Sisense

Publishes a live datamodel in Sisense.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/builds`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Publish Live Datamodel](https://developer.sisense.com/guides/restApi/datamodels.v2.html#publishing-live-datamodels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datamodelId` | body | `string` | yes | Live datamodel OID to publish. |
