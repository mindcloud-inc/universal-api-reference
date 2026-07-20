# Reorder Field with Clappia

Updates app field order in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/appdefinitionv2/reorderField`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Reorder Field](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `sourcePageIndex` | body | `number` | yes | Zero-based page index containing the field to move. |
| `targetPageIndex` | body | `number` | yes | Zero-based page index where the field should be moved. |
| `sourceSectionIndex` | body | `number` | yes | Zero-based section index containing the field to move. |
| `targetSectionIndex` | body | `number` | yes | Zero-based section index where the field should be moved. |
| `indexInTargetSection` | body | `number` | yes | Zero-based insertion index inside the target section. |
| `fieldName` | body | `string` | yes | Variable name of the field to move. |
