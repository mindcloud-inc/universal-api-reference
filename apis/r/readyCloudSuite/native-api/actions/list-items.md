# List Items with ReadyCloud Suite

Retrieves items from ReadyCloud Suite.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orgs/:orgPk/orders/:orderPk/boxes/:boxPk/items/`
- **Base URL:** `https://www.readycloud.com`
- **Official documentation:** [List Items](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-05-items.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boxPk` | path | `string` | yes | ReadyCloud box identifier. |
| `orderPk` | path | `string` | yes | ReadyCloud order identifier. |
| `orgPk` | path | `string` | yes | ReadyCloud organization identifier. |
