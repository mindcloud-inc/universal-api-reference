# Detect SQL Injection with Cloudmersive Security

Detects SQL injection threats in Cloudmersive Security.

## Endpoint

- **Method:** `POST`
- **Path:** `/security/threat-detection/content/sql-injection/detect/string`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Detect SQL Injection](https://api.cloudmersive.com/docs/security.asp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputText` | body | `string` | yes | Text input to scan for SQL injection attacks. |
