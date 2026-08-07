# Search Constituents Duplicate with BlackBaud

## Endpoint

- **Method:** `GET`
- **Path:** `constituent/v1/constituents/duplicatesearch`
- **Base URL:** `https://api.sky.blackbaud.com/`
- **Official documentation:** [Search Constituents Duplicate](https://developer.blackbaud.com/skyapi/renxt/constituent/entities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `last_name` | query | `string` | yes | Last name to use when checking for potential duplicate constituents. |
| `first_name` | query | `string` | no | First name to refine duplicate constituent matching. |
| `email` | query | `string` | no | Email address to refine duplicate constituent matching. |
