# Remove Account Unsubscribe with GMass

Deletes an address from your GMass unsubscribe list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/unsubscribes`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [Remove Account Unsubscribe](https://api.gmass.co/docs#tag/Unsubscribes/operation/Unsubscribes_DeleteUnsubscribe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAddress` | query | `string` | yes | Email address to remove from the account unsubscribe list. |
