# List Actor Versions with Apify

Retrieves actor versions for an Apify actor.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/acts/:actorId/versions`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [List Actor Versions](https://docs.apify.com/api/v2/act-versions-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actorId` | path | `string` | yes | The ID or username of the actor whose versions to list. |
