# Mirror Card To Card with Placker

## Endpoint

- **Method:** `POST`
- **Path:** `/card/:card/mirror/card`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Mirror Card To Card](https://placker.com/docs/api/paths/mirror.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card` | path | `number` | yes | Source card ID. |
| `list` | body | `number` | yes | Target list ID where the mirrored card will be created. |
| `position` | body | `number` | no | Optional position within the list. |
