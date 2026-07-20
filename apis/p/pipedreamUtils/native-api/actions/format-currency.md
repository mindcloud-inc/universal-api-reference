# Formatting - [Numbers] Format Currency with Pipedream Utils

Formats a number as currency in Pipedream Utils.

## Endpoint

- **Method:** `GET`
- **Base URL:** `https://pipedream.com`
- **Official documentation:** [Formatting - [Numbers] Format Currency](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/format-currency/format-currency.mjs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Number you would like to format as a currency. |
| `currency` | body | `string` | yes | Specify the currency to be used for formatting |
| `currencyFormat` | body | `string` | yes | Specify the format to be used for the currency formatting. Use the unicode currency symbol `¤` for special formatting options. [Formatting rules can be found here](http://www.unicode.org/reports/tr35/tr35-numbers.html#Number_Format_Patterns) |
