# Get Publication with Beehiiv

Retrieves a publication from Beehiiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Get Publication](https://developers.beehiiv.com/api-reference/publications/show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | Publication identifier (v2 format starts with pub_). |
| `expand` | query | `string` | no | Optional expansions for publication stats and related data. |
