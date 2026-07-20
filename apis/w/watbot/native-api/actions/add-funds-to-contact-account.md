# Add Funds To Contact Account with Watbot

Adds funds to a contact account in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/addFundsToContactAccount`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Add Funds To Contact Account](https://docs.watbot.ru/rabota-s-api/kontakty/bills)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | body | `number` | yes | ID of the contact account. |
| `amount` | body | `number` | yes | Amount in the minor currency unit. |
| `description` | body | `string` | yes | Transaction description. |
