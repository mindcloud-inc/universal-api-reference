# Retrieve Print-Ready File with Zakeke

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/designs/{designID}/outputfiles/{fileFormat}`
- **Base URL:** `https://api.zakeke.com`
- **Official documentation:** [Retrieve Print-Ready File](https://docs.zakeke.com/docs/API/designs-API#8-retrieve-print-ready-file-with-a-given-file-format)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `designID` | path | `string` | yes | Unique design identifier provided by Zakeke. |
| `fileFormat` | path | `string` | yes | Requested print-ready file format. |
