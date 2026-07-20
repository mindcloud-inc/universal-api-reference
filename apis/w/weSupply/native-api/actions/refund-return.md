# Refund Return with WeSupply

Issues a refund for a return in WeSupply.

## Endpoint

- **Method:** `POST`
- **Path:** `/returns/flow/refund/execute`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [Refund Return](https://documenter.getpostman.com/view/11859344/T17AiAYq#7bb2ff7a-8b80-4d47-bba9-5a3d9b6de866)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Comment` | body | `string` | no | Optional internal comment for the refund action. |
| `ItemQualities` | body | `string` | no | Optional item-quality payload for the refund action. |
| `Reference` | body | `string` | no | The WeSupply return reference to refund. |
