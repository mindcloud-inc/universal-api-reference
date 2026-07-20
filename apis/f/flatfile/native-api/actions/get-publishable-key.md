# Get Publishable Key with Flatfile

Retrieves a publishable key for a Flatfile environment.

## Endpoint

- **Method:** `GET`
- **Path:** `/auth/publishable-key`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [Get Publishable Key](https://reference.flatfile.com/api-reference/auth/get-publishable-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentId` | query | `string` | yes | Flatfile environment ID to fetch the publishable key for. |
