# Update Box with ReadyCloud Suite

Updates an existing box in ReadyCloud Suite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/orgs/:orgPk/orders/:orderPk/boxes/:boxPk/`
- **Base URL:** `https://www.readycloud.com`
- **Official documentation:** [Update Box](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-03-boxes.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boxPk` | path | `string` | yes | ReadyCloud box identifier. |
| `orderPk` | path | `string` | yes | ReadyCloud order identifier. |
| `orgPk` | path | `string` | yes | ReadyCloud organization identifier. |
