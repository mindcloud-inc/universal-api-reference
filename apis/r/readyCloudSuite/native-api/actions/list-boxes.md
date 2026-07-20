# List Boxes with ReadyCloud Suite

Retrieves boxes from ReadyCloud Suite.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orgs/:orgPk/orders/:orderPk/boxes/`
- **Base URL:** `https://www.readycloud.com`
- **Official documentation:** [List Boxes](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-03-boxes.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderPk` | path | `string` | yes | ReadyCloud order identifier. |
| `orgPk` | path | `string` | yes | ReadyCloud organization identifier. |
