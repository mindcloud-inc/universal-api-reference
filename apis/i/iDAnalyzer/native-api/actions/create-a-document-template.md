# Create a document template with ID Analyzer

Creates a document template in ID Analyzer.

## Endpoint

- **Method:** `POST`
- **Path:** `/contract`
- **Base URL:** `https://api2.idanalyzer.com`
- **Official documentation:** [Create a document template](https://developer.idanalyzer.com/reference/post-contract-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | HTML template content. |
| `name` | body | `string` | yes | Template name. |
