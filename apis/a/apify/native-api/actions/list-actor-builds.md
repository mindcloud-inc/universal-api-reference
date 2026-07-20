# List Actor Builds with Apify

Retrieves actor builds for an Apify actor.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/acts/:actorId/builds`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [List Actor Builds](https://docs.apify.com/api/v2/act-builds-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actorId` | path | `string` | yes | The ID or username of the actor whose builds to list. |
