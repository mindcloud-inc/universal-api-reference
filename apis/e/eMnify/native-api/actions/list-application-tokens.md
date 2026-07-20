# List Application Tokens with EMnify

Retrieves a list of application tokens from EMnify.

## Endpoint

- **Method:** `GET`
- **Path:** `/application_token`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [List Application Tokens](https://docs.emnify.com/developers/api/application-tokens/application-token-get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
