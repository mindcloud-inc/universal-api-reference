# Put Statement with Veracity Learning

Creates a single statement in Veracity Learning using a statement ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/statements`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [Put Statement](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `statementId` | query | `string` | yes | Exact xAPI statement UUID to store. |
| `statement` | body | `object` | yes | xAPI Statement object to store. |
