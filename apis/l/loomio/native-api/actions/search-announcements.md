# Search Announcements with Loomio

Finds announcements in Loomio by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/announcements/search`
- **Base URL:** `https://www.loomio.com/api/v1`
- **Official documentation:** [Search Announcements](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/announcements_controller.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | The announcement search query. |
