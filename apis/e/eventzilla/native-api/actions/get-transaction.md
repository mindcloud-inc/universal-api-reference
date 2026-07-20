# Get Transaction with Eventzilla

Retrieves a transaction from Eventzilla by checkout ID or reference.

## Endpoint

- **Method:** `GET`
- **Path:** `/transactions/:lookup`
- **Base URL:** `https://www.eventzillaapi.net/api/v2`
- **Official documentation:** [Get Transaction](https://developer.eventzilla.net/docs/#transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lookup` | path | `string` | yes | A checkout ID or order reference number. |
