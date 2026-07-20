# Create Record Call Log with NetHunt CRM

Creates a record call log in NetHunt CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/create-call-log/:recordId`
- **Base URL:** `https://nethunt.com/api/v1/zapier`
- **Official documentation:** [Create Record Call Log](https://nethunt.com/integration-api#create-call-log)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `duration` | body | `number` | no | Call log duration in minutes. |
| `recordId` | path | `string` | yes | Record ID to create the call log for. |
| `text` | body | `string` | yes | Call log text. |
| `time` | body | `date` | no | ISO-formatted UTC time when the call started. |
