# List Employee Time Off Requests with TalentHR

Retrieves an employee's time off requests from TalentHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/employees/:employee/time-off-requests`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [List Employee Time Off Requests](https://apidocs.talenthr.io/#a084bf09-87f6-4c1f-86d0-2d42f5944f35)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employee` | path | `number` | yes | TalentHR employee ID. |
| `limit` | query | `number` | no | Maximum number of requests to return. |
| `offset` | query | `number` | no | Number of requests to skip. |
| `sort` | query | `string` | no | Field to sort by. |
