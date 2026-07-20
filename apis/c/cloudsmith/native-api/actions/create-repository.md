# Create Repository with Cloudsmith

## Endpoint

- **Method:** `POST`
- **Path:** `/repos/:owner/`
- **Base URL:** `https://api.cloudsmith.io`
- **Official documentation:** [Create Repository](https://help.cloudsmith.io/reference/repos_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Namespace that will own the repository. |
| `name` | body | `string` | yes | Descriptive name for the repository. |
| `description` | body | `string` | no | Optional description of the repository. |
