# Protect PDF with XSS PDF Solutions

Creates a protected PDF in XSS PDF Solutions.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/32`
- **Base URL:** `https://api.xss-cross-service-solutions.com/solutions/solutions`
- **Official documentation:** [Protect PDF](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/#protect-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file to be protected with a password. |
| `userPass` | body | `string` | yes | The password to lock the PDF. |
