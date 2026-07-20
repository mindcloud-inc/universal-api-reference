# Get Voided Statement with Veracity Learning

Retrieves a voided statement from Veracity Learning by statement ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/statements`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [Get Voided Statement](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voidedStatementId` | query | `string` | yes | Id of the voided statement to fetch |
| `format` | query | `string` | no | Statement response format: exact, canonical, or ids |
| `attachments` | query | `boolean` | no | Include statement attachments in the response |
