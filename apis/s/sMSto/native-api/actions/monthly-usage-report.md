# Monthly Usage Report with SMS.to

Retrieves a monthly usage report from SMS.to.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/reports/monthly-usage`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Monthly Usage Report](https://developers.sms.to/#f1fe0830-0200-45ec-b81f-f09e3977a479)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billing_month` | body | `string` | yes | Billing month to report on. Format: YYYY-MM. |
| `product` | body | `list<string>` | no | Product to report usage for. Possible values: MESSAGING, VERIFY. Accepted values: `MESSAGING`, `VERIFY`. |
| `channel[]` | body | `array<string>` | no | Channels to include in the report. Possible values: SMS, VIBER, WHATSAPP, TELEGRAM. |
| `country[]` | body | `array<string>` | no | Destination country codes (ISO-3166-1 alpha-2). |
| `network` | body | `boolean` | no | Filter by network. |
