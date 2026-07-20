# Get Responses with Formbricks

Retrieves responses from Formbricks.

## Endpoint

- **Method:** `GET`
- **Path:** `/management/responses`
- **Base URL:** `https://app.formbricks.com/api/v2`
- **Official documentation:** [Get Responses](https://formbricks.com/docs/api-v2-reference/management-api--responses/get-responses)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `limit` | query | `number` | no |
| `skip` | query | `number` | no |
| `sortBy` | query | `string` | no |
| `order` | query | `string` | no |
| `startDate` | query | `date` | no |
| `endDate` | query | `date` | no |
| `filterDateField` | query | `string` | no |
| `surveyId` | query | `string` | no |
| `contactId` | query | `string` | no |
