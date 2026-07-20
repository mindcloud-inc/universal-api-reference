# Delete Link with Switchy.io

Deletes an existing link from Switchy.io by domain and ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/graphql`
- **Base URL:** `https://graphql.switchy.io`
- **Official documentation:** [Delete Link](https://developers.switchy.io/docs/overview/root-endpoint)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `domain` | body | `string` | yes |
| `id` | body | `string` | yes |
