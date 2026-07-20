# Create Block with Fingertip

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/pages/:pageId/blocks`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Create Block](https://docs.fingertip.com/openapi-specs/create-block)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | ID of the page to create a block in |
| `name` | body | `string` | yes | Name of the block |
| `kind` | body | `string` | yes | Type or category of the block |
| `componentBlockId` | body | `string` | yes | ID of the component block if this is an instance |
| `content` | body | `object` | no | Content of the block |
| `isComponent` | body | `boolean` | no | Whether this block is a component |
