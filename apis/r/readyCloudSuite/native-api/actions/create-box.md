# Create Box with ReadyCloud Suite

Creates a new box in ReadyCloud Suite.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/orgs/:orgPk/orders/:orderPk/boxes/`
- **Base URL:** `https://www.readycloud.com`
- **Official documentation:** [Create Box](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-03-boxes.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderPk` | path | `string` | yes | ReadyCloud order identifier. |
| `orgPk` | path | `string` | yes | ReadyCloud organization identifier. |
