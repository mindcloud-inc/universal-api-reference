# Get Domain with Switchy.io

Retrieves a domain from Switchy.io by name and owner ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/graphql`
- **Base URL:** `https://graphql.switchy.io`
- **Official documentation:** [Get Domain](https://developers.switchy.io/docs/guides/how-to-query)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `ownerId` | body | `string` | yes |
