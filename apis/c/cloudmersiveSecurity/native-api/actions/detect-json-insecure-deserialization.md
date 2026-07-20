# Detect JSON Insecure Deserialization with Cloudmersive Security

Detects JSON insecure deserialization attacks in Cloudmersive Security.

## Endpoint

- **Method:** `POST`
- **Path:** `/security/threat-detection/content/insecure-deserialization/json/detect/string`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Detect JSON Insecure Deserialization](https://api.cloudmersive.com/docs/security.asp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jsonText` | body | `string` | yes | JSON text input to scan for insecure deserialization attacks. |
