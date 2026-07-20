# Advanced Scan File for Viruses with Cloudmersive Virus Scan

Performs an advanced file virus scan with Cloudmersive Virus Scan.

## Endpoint

- **Method:** `POST`
- **Path:** `/virus/scan/file/advanced`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Advanced Scan File for Viruses](https://api.cloudmersive.com/docs/virus.asp#operation--virus-scan-file-advanced-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputFile` | body | `file` | yes | Input file to scan for viruses and advanced content threats. |
