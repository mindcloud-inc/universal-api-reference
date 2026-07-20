# Link WhatsApp Account with WhatsBoost

Links a WhatsApp account in WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/create/wa.link`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Link WhatsApp Account](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sid` | body | `number` | no | Optional WhatsApp server ID. If not provided, the system will automatically select the best available server from your package. You can get available server IDs from /get/wa.servers |
