# Scan File for Viruses with Cloudmersive Virus Scan

Scans a file for viruses with Cloudmersive Virus Scan.

## Endpoint

- **Method:** `POST`
- **Path:** `/virus/scan/file`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Scan File for Viruses](https://api.cloudmersive.com/docs/virus.asp#operation--virus-scan-file-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input file to scan for viruses. |
