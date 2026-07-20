# Format Currency with Formatting

Formats currency in the Formatting app.

## Endpoint

- **Method:** `POST`
- **Path:** `/post`
- **Base URL:** `https://postman-echo.com`
- **Official documentation:** [Format Currency](https://github.com/PipedreamHQ/pipedream/blob/master/components/formatting/actions/format-currency/format-currency.ts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `number` | yes | The number to format as currency. |
| `currency` | body | `string` | yes | The ISO currency code. |
| `locale` | body | `string` | no | The locale to use for formatting. |
