# Formatting - [Text] Extract Phone Number with Pipedream Utils

Extracts the first phone number in Pipedream Utils.

## Endpoint

- **Method:** `GET`
- **Base URL:** `https://pipedream.com`
- **Official documentation:** [Formatting - [Text] Extract Phone Number](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/extract-phone-number/extract-phone-number.mjs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | String from which you'd like to extract a phone number |
| `format` | body | `string` | yes | Choose a phone number format, or use a custom string representing a [Regular Expression](https://www.w3schools.com/js/js_regexp.asp) (without the forward slashes) |
