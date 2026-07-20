# List Candidates with TalentHR

Retrieves candidates from TalentHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/ats-applicants`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [List Candidates](https://apidocs.talenthr.io/#94264a53-3741-4608-9f3d-87682bb2ee42)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of candidates to return. |
| `offset` | query | `number` | no | Number of candidates to skip before returning results. |
| `search` | query | `string` | no | Free-text search term for candidates. |
| `sort` | query | `string` | no | Field used to sort candidate results. |
| `order` | query | `string` | no | Sort direction for candidate results. |
| `pool` | query | `boolean` | no | Whether to restrict results to the talent pool. |
