# Update Work Type with Envoice

Updates an existing work type in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `worktype/update`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Update Work Type](https://github.com/EmitKnowledge/Envoice/blob/master/work-type.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `number` | yes | Work type ID. |
| `Title` | body | `string` | yes | Work type title. |
