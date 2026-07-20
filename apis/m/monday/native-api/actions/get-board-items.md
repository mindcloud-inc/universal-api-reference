# Get Board Items with Monday

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.monday.com/v2/`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardId` | body | `number` | yes | — |
| `afterDate` | body | `date` | no | Filter items updated after this date |
