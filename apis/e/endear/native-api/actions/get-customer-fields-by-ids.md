# Get Customer Fields By IDs with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Get Customer Fields By IDs](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.ids[]` | body | `array<string>` | yes | Ids for the Endear GraphQL operation. |
