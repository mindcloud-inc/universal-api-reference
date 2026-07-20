# Get Statement with Veracity Learning

Retrieves a statement from Veracity Learning by statement ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/statements`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [Get Statement](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `statementId` | query | `string` | yes | Id of the statement to fetch |
| `format` | query | `string` | no | Statement response format: exact, canonical, or ids |
| `attachments` | query | `boolean` | no | Include statement attachments in the response |
