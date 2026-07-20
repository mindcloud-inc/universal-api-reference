# Identify Person with Encharge Ingest

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://ingest.encharge.io/v1`
- **Official documentation:** [Identify Person](https://docs.encharge.io/getting-started/connecting-your-app-to-encharge/ingest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | body | `object` | yes | JSON object for the user to create or update. Include at least `email` or `userId`. |
| `properties` | body | `object` | no | JSON object with person properties to update in Encharge. |
| `sourceIp` | body | `string` | no | End-user IP address, if available. |
