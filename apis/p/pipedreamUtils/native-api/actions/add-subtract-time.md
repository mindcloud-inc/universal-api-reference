# Formatting - [Date/Time] Add/Subtract Time with Pipedream Utils

Adds or subtracts time from a date in Pipedream Utils.

## Endpoint

- **Method:** `GET`
- **Base URL:** `https://pipedream.com`
- **Official documentation:** [Formatting - [Date/Time] Add/Subtract Time](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/add-subtract-time/add-subtract-time.mjs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputDate` | body | `string` | yes | A valid date string, in the format selected in Input Format. |
| `inputFormat` | body | `string` | no | The format of the input date string. If omitted, the parser will try to infer it. |
| `operation` | body | `string` | yes | Whether to add or subtract time. |
| `duration` | body | `string` | yes | The duration for the operation. You can use the shorthand duration, for example: `1s`, `1m`, `1h`, `1d`, `1w`, `1y` equal one second, minute, hour, day, week, and year respectively |
| `outputFormat` | body | `string` | yes | — |
