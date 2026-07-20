# List Job Position Applicants with TalentHR

Retrieves applicants for a TalentHR job position.

## Endpoint

- **Method:** `GET`
- **Path:** `/job-positions/:jobPosition/ats-applicants`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [List Job Position Applicants](https://apidocs.talenthr.io/#aa58799a-5b48-43f2-9664-3ec0787083d9)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobPosition` | path | `number` | yes | TalentHR job position ID. |
| `limit` | query | `number` | no | Maximum number of applicants to return. |
| `offset` | query | `number` | no | Number of applicants to skip. |
| `order` | query | `string` | no | Sort direction. |
| `sort` | query | `string` | no | Field to sort by. |
| `search` | query | `string` | no | Search applicants. |
