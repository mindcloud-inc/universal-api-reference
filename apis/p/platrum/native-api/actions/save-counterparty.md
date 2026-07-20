# Save counterparty with Platrum

Creates or updates a counterparty in Platrum.

## Endpoint

- **Method:** `POST`
- **Path:** `/fintransaction/api/counterparty/save`
- **Base URL:** `https://3e8e7be.platrum.com`
- **Official documentation:** [Save counterparty](http://api.docs.platrum.ru/modules/finance/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Counterparty address. |
| `comment` | body | `string` | no | Counterparty comment. |
| `company_name` | body | `string` | no | Company name. |
| `email` | body | `string` | no | Counterparty email. |
| `id` | body | `number` | no | Counterparty ID for updates. |
| `name` | body | `string` | no | Counterparty name. |
| `phone` | body | `string` | no | Counterparty phone. |
