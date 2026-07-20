# Mutate Insight with LogSnag

## Endpoint

- **Method:** `PATCH`
- **Path:** `/insight`
- **Base URL:** `https://api.logsnag.com/v1`
- **Official documentation:** [Mutate Insight](https://docs.logsnag.com/api-reference/insight-mutate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Project name in LogSnag. |
| `title` | body | `string` | yes | Insight title. |
| `value` | body | `object` | yes | Mutation object for the insight value. |
| `icon` | body | `string` | no | Single emoji or emoji shortcode. |
