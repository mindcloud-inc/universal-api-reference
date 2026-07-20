# Remove Unsubscribed Domain with GMass

Deletes an unsubscribed domain from GMass.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/unsubscribes/domain/:domain`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [Remove Unsubscribed Domain](https://api.gmass.co/docs#tag/Unsubscribes/operation/Unsubscribes_DeleteUnsubscribeDomain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain to remove from the account unsubscribe domain list. |
