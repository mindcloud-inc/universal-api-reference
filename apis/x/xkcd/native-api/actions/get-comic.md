# Get Comic with Xkcd

Retrieves comic metadata from Xkcd by comic number.

## Endpoint

- **Method:** `GET`
- **Path:** `/:comicNumber/info.0.json`
- **Base URL:** `https://xkcd.com`
- **Official documentation:** [Get Comic](https://xkcd.com/json.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comicNumber` | path | `number` | yes | The xkcd comic number to fetch, as documented in the /614/info.0.json example. |
