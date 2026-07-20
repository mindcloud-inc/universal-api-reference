# Get WhatsApp information after linking with WhatsBoost

Retrieves WhatsApp account info after linking in WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/get/wa.info`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Get WhatsApp information after linking](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | body | `string` | yes | The token string you got from create WhatsApp QRCode |
