# Formatting - [Date/Time] Compare Dates with Pipedream Utils

Compares two dates and their duration in Pipedream Utils.

## Endpoint

- **Method:** `GET`
- **Base URL:** `https://pipedream.com`
- **Official documentation:** [Formatting - [Date/Time] Compare Dates](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/compare-dates/compare-dates.mjs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputDate` | body | `string` | yes | Enter start date string, in the format defined in `Input Format`. If the start date is after the end date, these dates will be swapped and in the output `datesSwapped` will be set to `true`. |
| `endDate` | body | `string` | yes | Enter end date string, in the format defined in `Input Format`. Timezone is assumed the same for both dates if not explicitly set. |
| `inputFormat` | body | `string` | no | The format of the input date strings. If omitted, the parser will try to infer it. |
