# Create Statement By ID with GrassBlade LRS

Stores a statement by ID in GrassBlade LRS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/statements`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Create Statement By ID](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresput)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `statementId` | query | `string` | yes | Statement ID to store. |
| `actor.mbox` | body | `string` | yes | Actor mailbox IRI. |
| `actor.name` | body | `string` | no | Actor display name. |
| `verb.id` | body | `string` | yes | Verb ID IRI. |
| `object.id` | body | `string` | yes | Statement object activity ID. |
| `object.objectType` | body | `string` | no | Statement object type when required. |
| `context.registration` | body | `string` | no | Registration UUID. |
