# List Characters By House with Harry Potter

Retrieves Harry Potter characters by Hogwarts house.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/characters/house/:house`
- **Base URL:** `https://hp-api.onrender.com`
- **Official documentation:** [List Characters By House](https://hp-api.onrender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `house` | path | `string` | yes | Hogwarts house to filter by. Accepted values: `0`, `1`, `2`, `3`. |
