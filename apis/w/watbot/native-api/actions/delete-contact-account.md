# Delete Contact Account with Watbot

Deletes an existing contact account from Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/deleteContactAccount`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Delete Contact Account](https://docs.watbot.ru/rabota-s-api/kontakty/bills)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | body | `number` | yes | ID of the contact account to delete. |
