# Topia: Native API Reference

A consolidated summary of Topia's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.topia.io/api-docs
- **OpenAPI specification:** https://api.topia.io/api-docs/swagger.yaml
- **API base URL:** `https://api.topia.io/api`

## Authentication

### API Key

Authenticate with a Topia-generated API key sent as the raw value of the authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
authorization: <apiKey>
```

[Official authentication documentation](https://resources.topia.io/topia-public-api)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Enter World](actions/enter-world.md) | `GET /v1/world/:urlSlug/enter-world` | [docs](https://api.topia.io/api-docs/paths/v1/enterWorld.yaml) |
| [Get Dropped Asset](actions/get-dropped-asset.md) | `GET /v1/world/:urlSlug/assets/:id` | [docs](https://api.topia.io/api-docs/paths/v1/droppedAsset.yaml) |
| [Get Dropped Asset by Unique Name](actions/get-dropped-asset-by-unique-name.md) | `GET /v1/world/:urlSlug/asset-by-unique-name/:uniqueName` | [docs](https://api.topia.io/api-docs/paths/v1/droppedAssetByUniqueName.yaml) |
| [Get Inventory Item](actions/get-inventory-item.md) | `GET /v1/inventory/:itemId` | [docs](https://api.topia.io/api-docs/paths/v1/getInventoryItem.yaml) |
| [Get Media](actions/get-media.md) | `GET /v1/media/:urlSlug` | [docs](https://api.topia.io/api-docs/paths/v1/media.yaml) |
| [Get Scene](actions/get-scene.md) | `GET /v1/scenes/:sceneId` | [docs](https://api.topia.io/api-docs/paths/v1/scene.yaml) |
| [Get Visitor](actions/get-visitor.md) | `GET /v1/world/:urlSlug/visitors/:visitorId` | [docs](https://api.topia.io/api-docs/paths/v1/visitor.yaml) |
| [Get Visitor Data Object](actions/get-visitor-data-object.md) | `GET /v1/world/:urlSlug/visitors/:visitorId/get-data-object` | [docs](https://api.topia.io/api-docs/paths/v1/getVisitorDataObject.yaml) |
| [Get Visitor Inventory Item](actions/get-visitor-inventory-item.md) | `GET /v1/world/:urlSlug/visitors/:visitorId/get-visitor-inventory-items/:itemId` | [docs](https://api.topia.io/api-docs/paths/v1/getVisitorSpecificInventoryItem.yaml) |
| [Get Webhook](actions/get-webhook.md) | `GET /v1/world/:urlSlug/webhooks/:webhookId` | [docs](https://api.topia.io/api-docs/paths/v1/webhook.yaml) |
| [Get World Data Object](actions/get-world-data-object.md) | `GET /v1/world/:urlSlug/get-data-object` | [docs](https://api.topia.io/api-docs/paths/v1/getWorldDataObject.yaml) |
| [Get World Details](actions/get-world-details.md) | `GET /v1/world/:urlSlug/world-details` | [docs](https://api.topia.io/api-docs/paths/v1/world.yaml) |
| [List Admin Worlds](actions/list-admin-worlds.md) | `GET /v1/user/admin-worlds` | [docs](https://api.topia.io/api-docs/paths/v1/adminWorlds.yaml) |
| [List Avatars](actions/list-avatars.md) | `GET /v1/avatars/:profileId` | [docs](https://api.topia.io/api-docs/paths/v1/avatars.yaml) |
| [List Dropped Assets](actions/list-dropped-assets.md) | `GET /v1/world/:urlSlug/assets` | [docs](https://api.topia.io/api-docs/paths/v1/droppedAssets.yaml) |
| [List Dropped Assets by Scene Drop ID](actions/list-dropped-assets-by-scene-drop-id.md) | `GET /v1/world/:urlSlug/assets-with-scene-drop-id/:sceneDropId` | [docs](https://api.topia.io/api-docs/paths/v1/droppedAssetsBySceneDropId.yaml) |
| [List Expressions](actions/list-expressions.md) | `GET /v1/expressions` | [docs](https://api.topia.io/api-docs/paths/v1/expressions.yaml) |
| [List Interactive Dropped Assets](actions/list-interactive-dropped-assets.md) | `GET /v1/world/:urlSlug/interactive-dropped-assets` | [docs](https://api.topia.io/api-docs/paths/v1/interactiveDroppedAssets.yaml) |
| [List Interactive Worlds](actions/list-interactive-worlds.md) | `GET /v1/user/interactive-worlds` | [docs](https://api.topia.io/api-docs/paths/v1/interactiveWorlds.yaml) |
| [List Inventory Items](actions/list-inventory-items.md) | `GET /v1/inventory` | [docs](https://api.topia.io/api-docs/paths/v1/getInventoryItems.yaml) |
| [List My Assets](actions/list-my-assets.md) | `GET /v1/assets/my-assets` | [docs](https://api.topia.io/api-docs/paths/v1/myAssets.yaml) |
| [List My Scenes](actions/list-my-scenes.md) | `GET /v1/scenes/my-scenes` | [docs](https://api.topia.io/api-docs/paths/v1/scenes.yaml) |
| [List Topia Assets](actions/list-topia-assets.md) | `GET /v1/assets/topia-assets` | [docs](https://api.topia.io/api-docs/paths/v1/topiaAssets.yaml) |
| [List Topia Scenes](actions/list-topia-scenes.md) | `GET /v1/scenes/topia-scenes` | [docs](https://api.topia.io/api-docs/paths/v1/topiaScenes.yaml) |
| [List Visitor Inventory Items](actions/list-visitor-inventory-items.md) | `GET /v1/world/:urlSlug/visitors/:visitorId/get-visitor-inventory-items` | [docs](https://api.topia.io/api-docs/paths/v1/getVisitorInventoryItems.yaml) |
| [List Visitors](actions/list-visitors.md) | `GET /v1/world/:urlSlug/visitors` | [docs](https://api.topia.io/api-docs/paths/v1/visitors.yaml) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/world/:urlSlug/webhooks` | [docs](https://api.topia.io/api-docs/paths/v1/webhooks.yaml) |
| [List World Scenes](actions/list-world-scenes.md) | `GET /v1/world/:urlSlug/scenes` | [docs](https://api.topia.io/api-docs/paths/v1/sceneDropIds.yaml) |
| [List World Scenes With Dropped Assets](actions/list-world-scenes-with-dropped-assets.md) | `GET /v1/world/:urlSlug/scenes-with-dropped-assets` | [docs](https://api.topia.io/api-docs/paths/v1/sceneWithDroppedAssets.yaml) |
| [List Worlds](actions/list-worlds.md) | `GET /v1/user/worlds` | [docs](https://api.topia.io/api-docs/paths/v1/userWorlds.yaml) |
