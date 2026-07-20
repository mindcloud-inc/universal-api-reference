# Create a hosted Docupass flow with ID Analyzer

Creates a hosted Docupass flow in ID Analyzer.

## Endpoint

- **Method:** `POST`
- **Path:** `/docupass`
- **Base URL:** `https://api2.idanalyzer.com`
- **Official documentation:** [Create a hosted Docupass flow](https://developer.idanalyzer.com/reference/post-docupass)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mode` | body | `number` | yes | Docupass flow mode. |
| `profile` | body | `string` | yes | KYC profile ID configured for Docupass. |
| `version` | body | `string` | yes | Docupass version. |
