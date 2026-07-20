# Get Order Links with WeSupply

Retrieves WeSupply order links for external order IDs.

## Endpoint

- **Method:** `GET`
- **Path:** `/authLinks`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [Get Order Links](https://documenter.getpostman.com/view/11859344/T17AiAYq#f0995f02-67c2-4909-bd67-b8681eb0ce65)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OrderExternalOrderIDs` | query | `string` | no | Comma-separated external order IDs to convert into direct WeSupply order links. |
