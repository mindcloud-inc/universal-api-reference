# Create Collection with Underdog Protocol

Creates a new collection in Underdog Protocol.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/collections`
- **Base URL:** `https://dev.underdogprotocol.com`
- **Official documentation:** [Create Collection](https://docs.underdogprotocol.com/resources/v1/collections/create-a-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for you NFT Collection |
| `description` | body | `string` | yes | Description for your NFT Collection |
| `image` | body | `string` | yes | URL pointing to an image for your NFT Collection |
| `attributes` | body | `object` | no | Key-value pairs where the key is the attribute name and the value is the attribute value. |
