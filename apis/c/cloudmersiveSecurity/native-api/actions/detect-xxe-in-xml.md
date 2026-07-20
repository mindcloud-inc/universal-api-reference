# Detect XXE in XML with Cloudmersive Security

Detects XXE threats in XML with Cloudmersive Security.

## Endpoint

- **Method:** `POST`
- **Path:** `/security/threat-detection/content/xxe/detect/xml/string`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Detect XXE in XML](https://api.cloudmersive.com/docs/security.asp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `xmlText` | body | `string` | yes | XML text input to scan for XML External Entity attacks. |
