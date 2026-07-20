# Detect Headers with WhatIsMyBrowser

Retrieves browser and device details from WhatIsMyBrowser using request headers.

## Endpoint

- **Method:** `POST`
- **Path:** `/detect`
- **Base URL:** `https://api.whatismybrowser.com/api/v3`
- **Official documentation:** [Detect Headers](https://developers.whatismybrowser.com/api/docs/v3/integration-guide/detect/requests/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `headers[]` | body | `array<object>` | yes | Ordered list of visitor HTTP headers. Each item should include name and value fields, preserving the order received by your server. |
