# Detect Threats in Text with Cloudmersive Security

Detects threats in text with Cloudmersive Security.

## Endpoint

- **Method:** `POST`
- **Path:** `/security/threat-detection/content/automatic/detect/string`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Detect Threats in Text](https://api.cloudmersive.com/docs/security.asp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputText` | body | `string` | yes | User-facing text input to scan for SQLI, XSS, XXE, SSRF, and JSON insecure deserialization threats. |
