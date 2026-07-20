# Get Actor Build with Apify

Retrieves an actor build from Apify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/acts/:actorId/builds/:buildId`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [Get Actor Build](https://docs.apify.com/api/v2/act-build-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actorId` | path | `string` | yes | The ID or username of the actor that owns the build. |
| `buildId` | path | `string` | yes | The ID of the build to retrieve. |
