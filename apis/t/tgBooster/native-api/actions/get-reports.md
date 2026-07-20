# Get Reports with TgBooster

Retrieves custom campaign reports from a TgBooster cabinet.

## Endpoint

- **Method:** `POST`
- **Path:** `/cabinet/{CabinetId}/reports`
- **Base URL:** `https://api.tgbooster.ru/api`
- **Official documentation:** [Get Reports](https://tgbooster.gitbook.io/tgbooster/api/api-metody#poluchenie-otchetov)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CabinetId` | path | `number` | yes | Cabinet ID returned by List Cabinets. |
| `groups[date][day]` | body | `boolean` | no | Group report rows by day. |
| `groups[date][week]` | body | `boolean` | no | Group report rows by week. |
| `groups[ads][company]` | body | `boolean` | no | Group report rows by campaign. |
| `groups[ads][ad]` | body | `boolean` | no | Group report rows by ad. |
| `groups[ads][ad_url]` | body | `boolean` | no | Group report rows by ad URL. |
| `filters[company][]` | body | `array<number>` | no | Campaign IDs to include in the report. Send multiple values as a array. |
| `filters[dates][]` | body | `array<date>` | no | Two report dates: start date and end date. Send multiple values as a array. |
| `metrics[views]` | body | `boolean` | no | Include views metric. |
| `metrics[clicks]` | body | `boolean` | no | Include clicks metric. |
| `metrics[joins]` | body | `boolean` | no | Include joins metric. |
| `metrics[spent]` | body | `boolean` | no | Include spent metric. |
| `metrics[ctr]` | body | `boolean` | no | Include CTR metric. |
| `metrics[cv]` | body | `boolean` | no | Include conversion from views to joins. |
| `metrics[cpc]` | body | `boolean` | no | Include CPC metric. |
| `metrics[cps]` | body | `boolean` | no | Include CPS metric. |
