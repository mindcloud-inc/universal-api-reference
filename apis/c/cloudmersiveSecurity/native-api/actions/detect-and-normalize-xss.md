# Detect and Normalize XSS with Cloudmersive Security

Detects and normalizes XSS threats in Cloudmersive Security.

## Endpoint

- **Method:** `POST`
- **Path:** `/security/threat-detection/content/xss/detect/string`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Detect and Normalize XSS](https://api.cloudmersive.com/docs/security.asp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputText` | body | `string` | yes | Text input to scan and normalize for cross-site scripting attacks. |
