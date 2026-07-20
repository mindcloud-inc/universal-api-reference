# List Members with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/Panel/v3/ReadMemberList`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [List Members](https://developer.survalyzer.com/knowledge-base/code-examples/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interviewsRequired` | body | `string` | no | Whether interview data should be included. |
| `page` | body | `string` | no | 1-based results page number. |
| `pageSize` | body | `string` | no | Maximum number of records to return. |
| `panelId` | body | `string` | no | Panel identifier to read members from. |
