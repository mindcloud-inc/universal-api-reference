# Publish Insight with LogSnag

## Endpoint

- **Method:** `POST`
- **Path:** `/insight`
- **Base URL:** `https://api.logsnag.com/v1`
- **Official documentation:** [Publish Insight](https://docs.logsnag.com/api-reference/insight)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Project name in LogSnag. |
| `title` | body | `string` | yes | Insight title. |
| `value` | body | `string` | yes | Insight value. |
| `icon` | body | `string` | no | Single emoji or emoji shortcode. |
