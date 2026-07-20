# Create Playground with Recommand

Creates a new playground in Recommand.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/playgrounds`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Create Playground](https://recommand.eu/en/reference/playgrounds/create-playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Playground name |
| `useTestNetwork` | body | `boolean` | no | Whether to use the Peppol Test Network |
