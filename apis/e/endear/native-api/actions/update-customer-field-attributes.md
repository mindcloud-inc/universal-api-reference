# Update Customer Field Attributes with Endear

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.endearhq.com`
- **Official documentation:** [Update Customer Field Attributes](https://docs.endearhq.com/docs/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | Id for the Endear GraphQL operation. |
| `variables.key` | body | `string` | yes | Key for the Endear GraphQL operation. |
| `variables.changes[]` | body | `array<object>` | yes | Changes for the Endear GraphQL operation. |
