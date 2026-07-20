# Disassociate Repository Label with Socket

Disassociates a repository label from a Socket repository.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:org_slug/repos/labels/:label_id/disassociate`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Disassociate Repository Label](https://docs.socket.dev/reference/disassociateorgrepolabel)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `label_id` | path | `string` | yes |
