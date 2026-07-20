# Associate Repository Label with Socket

Associates a repository label with a Socket repository.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:org_slug/repos/labels/:label_id/associate`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Associate Repository Label](https://docs.socket.dev/reference/associateorgrepolabel)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `label_id` | path | `string` | yes |
