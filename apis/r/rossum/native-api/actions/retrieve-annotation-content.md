# Retrieve Annotation Content with Rossum

Retrieves annotation content from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/annotations/:annotationID/content`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Retrieve Annotation Content](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotationID` | path | `number` | yes | ID of the annotation whose datapoint tree should be retrieved. |
