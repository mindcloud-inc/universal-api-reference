# List Project Items By Quadrant with Priority Matrix

Retrieves project items from Priority Matrix by quadrant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/project/:idd/items/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [List Project Items By Quadrant](https://sync.appfluence.com/developer/guide/#common-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idd` | path | `number` | yes | Project IDD. |
| `quadrant` | query | `number` | yes | Quadrant number: 0 top-left, 1 top-right, 2 bottom-left, 3 bottom-right. |
