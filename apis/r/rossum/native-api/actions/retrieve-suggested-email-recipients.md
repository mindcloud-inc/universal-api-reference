# Retrieve Suggested Email Recipients with Rossum

Retrieves suggested email recipients for an annotation in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/annotations/suggested_recipients`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Retrieve Suggested Email Recipients](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotations[]` | body | `array<string>` | yes | Annotation URLs to analyze for suggested recipients. |
