# Get Member Follow with Invision Community

## Endpoint

- **Method:** `GET`
- **Path:** `/core/members/:id/follows/:followKey`
- **Base URL:** `{communityBaseUrl}/api`
- **Official documentation:** [Get Member Follow](https://invisioncommunity.com/developers/rest-api/index/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Member identifier. |
| `followKey` | path | `string` | yes | Follow identifier. |
