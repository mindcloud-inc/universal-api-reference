# Insert Object Type with Rillion Prime Web Service

Insert an accounting object type (coding dimension) into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ObjectType` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, ObjectType section. |
| `ObjectType.ObjectTypeNo` | body | `number` | yes | Object type number (1-8) |
| `ObjectType.Name` | body | `string` | yes | Object type name |
| `ObjectType.ExternalId` | body | `string` | no | — |
| `ObjectType.ExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
