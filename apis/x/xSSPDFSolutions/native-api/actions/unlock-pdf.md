# Unlock PDF with XSS PDF Solutions

Creates an unlocked PDF in XSS PDF Solutions.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/33`
- **Base URL:** `https://api.xss-cross-service-solutions.com/solutions/solutions`
- **Official documentation:** [Unlock PDF](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/#unlock-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The locked PDF file to be unlocked. |
| `password` | body | `string` | yes | The password to unlock the protected PDF. |
