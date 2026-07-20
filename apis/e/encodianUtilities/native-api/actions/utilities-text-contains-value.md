# Utilities - Text Contains Value with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/TextContainsValue`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Text Contains Value](https://support.encodian.com/hc/en-gb/articles/10515175130012/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text to validate |
| `value` | body | `string` | yes | The value to check is contained within the 'Text' value |
| `ignoreCase` | body | `boolean` | no | Set whether text case should be ignored when validating the 'Text' value |
| `comparisonConfiguration` | body | `string` | no | Specifies the rules to be used when processing the text values provided Accepted values: `0`, `1`, `2`. |
| `cultureName` | body | `string` | no | Change the thread culture used to process the request |
