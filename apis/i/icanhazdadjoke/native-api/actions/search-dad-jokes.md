# Search Dad Jokes with icanhazdadjoke

Finds dad jokes in icanhazdadjoke by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://icanhazdadjoke.com`
- **Official documentation:** [Search Dad Jokes](https://icanhazdadjoke.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | no | Optional search term to use when searching dad jokes. |
