# Create Buyer with Turis

Creates a new buyer in Turis.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/v1/buyers`
- **Base URL:** `https://{tenant}.turis.app`
- **Official documentation:** [Create Buyer](https://documenter.getpostman.com/view/16452985/TzkyP1Er)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Buyer street address. |
| `company_id` | body | `number` | yes | Company ID the buyer belongs to. |
| `email` | body | `string` | no | Buyer email address. |
| `first_name` | body | `string` | no | Buyer first name. |
| `invite_buyer` | body | `boolean` | no | Whether to send a buyer invite. |
| `language_id` | body | `number` | no | Buyer language identifier. |
