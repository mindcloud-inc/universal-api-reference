# Get credit card icon with Appwrite

Retrieves a credit card icon from Appwrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/avatars/credit-cards/{code}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get credit card icon](https://appwrite.io/docs/references/cloud/server-rest/avatars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `file` | yes | Credit Card Code. Possible values: amex, argencard, cabal, cencosud, diners, discover, elo, hipercard, jcb, mastercard, naranja, targeta-shopping, unionpay, visa, mir, maestro, rupay. |
| `width` | query | `number` | no | Image width. Pass an integer between 0 to 2000. Defaults to 100. |
| `height` | query | `number` | no | Image height. Pass an integer between 0 to 2000. Defaults to 100. |
| `quality` | query | `number` | no | Image quality. Pass an integer between 0 to 100. Defaults to keep existing image quality. |
