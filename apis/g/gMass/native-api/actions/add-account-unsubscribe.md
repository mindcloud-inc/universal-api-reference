# Add Account Unsubscribe with GMass

Adds an address to your GMass unsubscribe list.

## Endpoint

- **Method:** `POST`
- **Path:** `/unsubscribes`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [Add Account Unsubscribe](https://api.gmass.co/docs#tag/Unsubscribes/operation/Unsubscribes_AddUnsubscribe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAddress` | body | `string` | yes | Email address to add to the account-wide unsubscribe list. |
