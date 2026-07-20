# Validate a WhatsApp phone number with WhatsBoost

Validates a WhatsApp phone number in WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/whatsapp`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Validate a WhatsApp phone number](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unique` | body | `string` | yes | WhatsApp Unique ID |
| `phone` | body | `string` | yes | E.164 formatted phone number |
