# Add Section with Clappia

Creates a new app section in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/appdefinitionv2/addSection`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Add Section](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `sectionIndex` | body | `number` | yes | Zero-based section index where the new section should be inserted. |
| `pageIndex` | body | `number` | yes | Zero-based page index where the section belongs. |
| `sectionName` | body | `string` | yes | Name of the new section. |
