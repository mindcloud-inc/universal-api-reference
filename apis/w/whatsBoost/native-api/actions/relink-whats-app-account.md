# Relink WhatsApp Account with WhatsBoost

Relinks a WhatsApp account in WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/create/wa.relink`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Relink WhatsApp Account](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sid` | body | `number` | no | Optional WhatsApp server ID. If not provided, the system will automatically prefer the current server or select another available server from your package. You can get available server IDs from /get/wa.servers |
| `unique` | body | `string` | yes | The unique ID of the WhatsApp account you want to relink |
