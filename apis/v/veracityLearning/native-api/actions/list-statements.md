# List Statements with Veracity Learning

Retrieves statements from Veracity Learning.

## Endpoint

- **Method:** `GET`
- **Path:** `/statements`
- **Base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`
- **Official documentation:** [List Statements](https://xapi.ieee-saopen.org/standard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent` | query | `object` | no | Filter statements to a specific xAPI Agent JSON object. |
| `verb` | query | `string` | no | Filter statements by verb IRI. |
| `activity` | query | `string` | no | Filter statements by activity IRI. |
| `registration` | query | `string` | no | Filter statements by registration UUID. |
| `since` | query | `date` | no | Return statements stored after this timestamp. |
| `until` | query | `date` | no | Return statements stored before this timestamp. |
| `format` | query | `string` | no | Select the xAPI statement response format. |
| `attachments` | query | `boolean` | no | Include attachment content when supported. |
| `ascending` | query | `boolean` | no | Return statements in ascending stored order. |
| `relatedActivities` | query | `boolean` | no | Include statements related to the supplied activity hierarchy. |
| `relatedAgents` | query | `boolean` | no | Include statements related to the supplied agent hierarchy. |
