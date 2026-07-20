# Send Event with Encharge Ingest

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://ingest.encharge.io/v1`
- **Official documentation:** [Send Event](https://docs.encharge.io/getting-started/connecting-your-app-to-encharge/ingest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the event to record in Encharge. |
| `user` | body | `object` | yes | JSON object for the current user. Include at least `email` or `userId`. |
| `properties` | body | `object` | no | JSON object with event properties. |
| `sourceIp` | body | `string` | no | End-user IP address, if available. |
