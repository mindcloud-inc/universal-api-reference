# Cancel Return with WeSupply

Cancels an existing return in WeSupply.

## Endpoint

- **Method:** `POST`
- **Path:** `/returns/flow/cancelation/execute`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [Cancel Return](https://documenter.getpostman.com/view/11859344/T17AiAYq#7bb2ff7a-8b80-4d47-bba9-5a3d9b6de866)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Comment` | body | `string` | no | Optional internal comment for the cancelation action. |
| `Reference` | body | `string` | no | The WeSupply return reference to cancel. |
