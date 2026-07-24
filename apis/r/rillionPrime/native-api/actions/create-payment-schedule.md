# Create Payment Schedule with Rillion Prime Pay

## Endpoint

- **Method:** `POST`
- **Path:** `/payment/schedule`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Payment Schedule](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X-Correlation-ID` | header | `string` | no | — |
| `interval` | body | `list<string>` | yes | Interval type Accepted values: `Daily`, `Instant`, `Weekly`. |
| `intervalConfiguration` | body | `object` | no | Configuration for interval. Required when interval is Daily or Weekly. |
| `intervalConfiguration.time` | body | `string` | no | Time of day (HH:mm:ss). Required when interval is Daily or Weekly. |
| `intervalConfiguration.day` | body | `list<string>` | no | Day of week (required when interval is Weekly). Accepted values: `Friday`, `Monday`, `Thursday`, `Tuesday`, `Wednesday`. |
