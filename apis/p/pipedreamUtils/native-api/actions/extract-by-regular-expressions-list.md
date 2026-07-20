# Formatting - [Text] Extract by Regular Expressions List (Regex) with Pipedream Utils

Extracts matches from multiple regex patterns in Pipedream Utils.

## Endpoint

- **Method:** `GET`
- **Base URL:** `https://pipedream.com`
- **Official documentation:** [Formatting - [Text] Extract by Regular Expressions List (Regex)](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/extract-by-regular-expressions-list/extract-by-regular-expressions-list.mjs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key_0` | body | `string` | yes | The key where the extraction result for a regex will be stored |
| `input_0` | body | `string` | yes | The text you would like to find a pattern from |
| `regex_0` | body | `string` | yes | [Regular expression](https://www.w3schools.com/js/js_regexp.asp) |
