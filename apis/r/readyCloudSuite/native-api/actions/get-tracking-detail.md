# Get Tracking Detail with ReadyCloud Suite

Retrieves a tracking entry from ReadyCloud Suite.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orgs/:orgPk/orders/:orderPk/boxes/:boxPk/tracking/:trackingPk/`
- **Base URL:** `https://www.readycloud.com`
- **Official documentation:** [Get Tracking Detail](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-04-tracking.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boxPk` | path | `string` | yes | ReadyCloud box identifier. |
| `orderPk` | path | `string` | yes | ReadyCloud order identifier. |
| `orgPk` | path | `string` | yes | ReadyCloud organization identifier. |
| `trackingPk` | path | `string` | yes | ReadyCloud tracking event identifier. |
