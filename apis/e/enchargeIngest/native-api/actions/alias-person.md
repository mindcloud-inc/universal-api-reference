# Alias Person with Encharge Ingest

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://ingest.encharge.io/v1`
- **Official documentation:** [Alias Person](https://docs.encharge.io/getting-started/connecting-your-app-to-encharge/ingest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `previousUserId` | body | `string` | no | Existing userId before the alias change. |
| `previousEmail` | body | `string` | no | Existing email before the alias change. |
| `user` | body | `object` | yes | JSON object containing the new `email` and/or `userId` values. |
