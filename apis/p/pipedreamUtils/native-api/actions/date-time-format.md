# Formatting - [Date/Time] Format with Pipedream Utils

Formats a date string in Pipedream Utils.

## Endpoint

- **Method:** `GET`
- **Base URL:** `https://pipedream.com`
- **Official documentation:** [Formatting - [Date/Time] Format](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/date-time-format/date-time-format.mjs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputDate` | body | `string` | yes | A valid date string, in the format selected in Input Format. |
| `inputFormat` | body | `string` | no | The format of the input date string. If omitted, the parser will try to infer it. |
| `outputFormat` | body | `string` | yes | The format to convert the date to. For more examples on formatting, see the [Sugar Date Format](https://sugarjs.com/dates/#/Formatting) documentation. |
