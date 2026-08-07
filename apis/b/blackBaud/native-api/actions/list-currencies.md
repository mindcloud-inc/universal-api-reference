# List Currencies with BlackBaud

## Endpoint

- **Method:** `GET`
- **Path:** `alt-adnmg/currencies/list`
- **Base URL:** `https://api.sky.blackbaud.com/`
- **Official documentation:** [List Currencies](https://developer.sky.blackbaud.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeinactive` | query | `boolean` | no | Include inactive currencies. |
| `limit` | query | `number` | no | Maximum number of currencies to return. |
| `session_key` | query | `string` | no | Paging session key returned by Blackbaud for multi-page reads. |
| `infinity_session` | query | `string` | no | Blackbaud Infinity session identifier when required by the endpoint. |
| `more_rows_range_key` | query | `string` | no | Blackbaud cursor-like range key for additional rows. |
| `start_row_index` | query | `number` | no | Row index to start returning results from. |
