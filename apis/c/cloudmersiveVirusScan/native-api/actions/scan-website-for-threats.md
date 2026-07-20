# Scan Website for Threats with Cloudmersive Virus Scan

Scans a website for malicious content with Cloudmersive Virus Scan.

## Endpoint

- **Method:** `POST`
- **Path:** `/virus/scan/website`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Scan Website for Threats](https://api.cloudmersive.com/docs/virus.asp#operation--virus-scan-website-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Url` | body | `string` | yes | Website URL to scan for malicious content and threats. Must begin with http:// or https://. |
