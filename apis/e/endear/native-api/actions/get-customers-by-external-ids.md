# Get Customers By External IDs with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Get Customers By External IDs](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.integrationId` | body | `string` | yes | Integration Id for the Endear GraphQL operation. |
| `variables.externalIds[]` | body | `array<string>` | yes | External Ids for the Endear GraphQL operation. |
