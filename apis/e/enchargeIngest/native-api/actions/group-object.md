# Group Object with Encharge Ingest

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://ingest.encharge.io/v1`
- **Official documentation:** [Group Object](https://docs.encharge.io/getting-started/connecting-your-app-to-encharge/ingest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectType` | body | `string` | yes | Name of the custom object type to create or update, for example `company`. |
| `properties` | body | `object` | yes | JSON object with custom object fields. Include `id` or `externalId` when updating an existing object. |
| `user` | body | `object` | no | Optional JSON object containing `email` or `userId` when you want to associate the object with a person. |
