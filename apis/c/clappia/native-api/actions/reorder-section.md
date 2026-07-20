# Reorder Section with Clappia

Updates app section order in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/appdefinitionv2/reorderSection`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Reorder Section](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `sourcePageIndex` | body | `number` | yes | Zero-based page index containing the section to move. |
| `sourceSectionIndex` | body | `number` | yes | Zero-based source section index. |
| `targetPageIndex` | body | `number` | yes | Zero-based page index where the section should be moved. |
| `targetSectionIndex` | body | `number` | yes | Zero-based target section index. |
