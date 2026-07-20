# Utilities - Validate Email Address with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/ValidateEmailAddress`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Validate Email Address](https://support.encodian.com/hc/en-gb/articles/9588817792925)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAddress` | body | `string` | yes | The email address to verify |
| `regex` | body | `string` | yes | The regular expression used for validation |
