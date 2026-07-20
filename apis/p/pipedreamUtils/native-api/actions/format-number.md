# Formatting - [Numbers] Format Number with Pipedream Utils

Formats a number without rounding in Pipedream Utils.

## Endpoint

- **Method:** `GET`
- **Base URL:** `https://pipedream.com`
- **Official documentation:** [Formatting - [Numbers] Format Number](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/format-number/format-number.mjs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Number string you would like to format. |
| `inputDecimalMark` | body | `string` | no | The character the input uses to denote the decimal/fractional portion of the number. Defaults to period `.` |
| `toFormat` | body | `string` | yes | The format the number will be converted to. |
