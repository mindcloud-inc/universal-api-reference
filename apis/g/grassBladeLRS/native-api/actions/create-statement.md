# Create Statement with GrassBlade LRS

Stores a statement in GrassBlade LRS.

## Endpoint

- **Method:** `POST`
- **Path:** `/statements`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Create Statement](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtrespost)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actor.mbox` | body | `string` | yes | Agent mailbox IRI for the statement actor. |
| `actor.name` | body | `string` | no | Human-readable name for the statement actor. |
| `verb.id` | body | `string` | yes | Verb IRI for the statement. |
| `object.id` | body | `string` | yes | Activity IRI for the statement object. |
| `object.objectType` | body | `string` | no | Optional objectType for the Statement object, such as StatementRef when voiding another statement. |
| `context.registration` | body | `string` | no | Registration UUID to associate with the statement context. |
