# Withdraw Funds From Contact Account with Watbot

Withdraws funds from a contact account in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/withdrawFundsFromContactAccount`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Withdraw Funds From Contact Account](https://docs.watbot.ru/rabota-s-api/kontakty/bills)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | body | `number` | yes | ID of the contact account. |
| `amount` | body | `number` | yes | Amount in the minor currency unit. |
| `description` | body | `string` | yes | Transaction description. |
