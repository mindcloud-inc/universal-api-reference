# Create Contact Account with Watbot

Creates a new contact account in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/addContactAccount`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Create Contact Account](https://docs.watbot.ru/rabota-s-api/kontakty/bills)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID of an existing Watbot contact. |
| `currency` | query | `string` | yes | Three-letter ISO 4217 currency code. |
