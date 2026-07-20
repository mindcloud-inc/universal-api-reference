# List Rooms with ClassDo

Retrieves a list of rooms from ClassDo.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.classdo.com`
- **Official documentation:** [List Rooms](https://developer.classdo.com/schema/viewer.doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL query payload for ClassDo. |
| `variables` | body | `object` | no | Optional GraphQL variables object. |
