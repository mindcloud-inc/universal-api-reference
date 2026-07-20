# Get Token with Switchy.io

Retrieves a token from Switchy.io by UID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/graphql`
- **Base URL:** `https://graphql.switchy.io`
- **Official documentation:** [Get Token](https://developers.switchy.io/docs/guides/how-to-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | body | `string` | yes | UUID primary key for the token record |
