# Send Card with CardClan

Sends a personalized CardClan card by email.

## Endpoint

- **Method:** `POST`
- **Path:** `/integration/send-card`
- **Base URL:** `https://app.cardclan.io/api`
- **Official documentation:** [Send Card](https://docs.cardclan.io/api-reference/integration/actions/send-card)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card` | body | `string` | yes | Card ID to send. |
| `emailAccount` | body | `string` | no | Email account ID or CardClan for the default sender. |
| `integrationId` | body | `string` | yes | Integration configuration ID. |
| `mergeTags[]` | body | `array<object>` | yes | Array of merge tag objects with recipient data. |
