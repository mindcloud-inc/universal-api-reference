# Generate Profile JWT with Ayrshare

Generates a single sign-on JWT in Ayrshare.

## Endpoint

- **Method:** `POST`
- **Path:** `/profiles/generateJWT`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Generate Profile JWT](https://www.ayrshare.com/docs/apis/profiles/generate-jwt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileKey` | body | `string` | yes | Profile key to generate a JWT linking URL for. |
