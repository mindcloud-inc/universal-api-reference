# Search Dependencies with Socket

Finds dependencies used in Socket by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/dependencies/search`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Search Dependencies](https://docs.socket.dev/reference/searchdependencies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purls` | body | `list<string>` | no | PURLs to filter results with |
