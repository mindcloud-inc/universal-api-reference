# List Activities with lemlist

Retrieves your activity records from lemlist.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [List Activities](https://developer.lemlist.com/api-reference/endpoints/activities/get-many-activities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Filter by activity type. |
| `campaignId` | query | `string` | no | Filter by campaign ID. |
| `isFirst` | query | `boolean` | no | Filter for first activity only. |
| `leadId` | query | `string` | no | Filter by lead ID. |
