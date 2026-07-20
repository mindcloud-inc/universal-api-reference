# List Authenticated User Repositories with GitHub

Lists GitHub repositories for the authenticated user.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/repos`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Authenticated User Repositories](https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28#list-repositories-for-the-authenticated-user)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `visibility` | query | `string` | no | Repository visibility to return. Accepted values: `0`, `1`, `2`. |
| `affiliation` | query | `string` | no | Repository affiliation values to include. Accepted values: `0`, `1`, `2`. Send multiple values as a string separated by `,`. |
| `type` | query | `string` | no | Repository type to return. GitHub ignores this parameter when visibility or affiliation is supplied. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `since` | query | `string` | no | Only show repositories updated after this time (ISO 8601). |
| `before` | query | `string` | no | Only show repositories updated before this time (ISO 8601). |
