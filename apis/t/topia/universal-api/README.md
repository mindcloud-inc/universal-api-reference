# <img src="https://images.mindcloud.co/apps/icons/topia_1775150266076.png" alt="Topia logo" width="28" height="28"> Topia: Universal API

Access Topia worlds, scenes, assets, visitors, webhooks, media, and inventory through the Topia Public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/topia/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://topia.io
- **Vendor API docs:** https://api.topia.io/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Worlds](actions/list-worlds.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-worlds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Dropped Asset](actions/get-dropped-asset.md) | GET | Retrieves a dropped asset from a Topia world. |
| [Get Dropped Asset by Unique Name](actions/get-dropped-asset-by-unique-name.md) | GET | Finds a dropped asset in Topia by unique name. |
| [Get Media](actions/get-media.md) | GET | Retrieves media uploaded by a Topia world owner. |
| [List Avatars](actions/list-avatars.md) | GET | Retrieves available avatars from Topia. |
| [List Dropped Assets](actions/list-dropped-assets.md) | GET | Retrieves dropped assets from a Topia world. |
| [List Dropped Assets by Scene Drop ID](actions/list-dropped-assets-by-scene-drop-id.md) | GET | Retrieves dropped assets in Topia by scene drop ID. |
| [List Expressions](actions/list-expressions.md) | GET | Retrieves available expressions from the Topia catalog. |
| [List Interactive Dropped Assets](actions/list-interactive-dropped-assets.md) | GET | Retrieves interactive dropped assets from a Topia world. |
| [List My Assets](actions/list-my-assets.md) | GET | Retrieves assets owned by your Topia account. |
| [List Topia Assets](actions/list-topia-assets.md) | GET | Retrieves Topia-provided assets from the shared library. |

### Inventory Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory Item](actions/get-inventory-item.md) | GET | Retrieves an inventory item from Topia. |
| [Get Visitor Inventory Item](actions/get-visitor-inventory-item.md) | GET | Retrieves a specific visitor inventory item from Topia. |
| [List Inventory Items](actions/list-inventory-items.md) | GET | Retrieves inventory items from Topia. |
| [List Visitor Inventory Items](actions/list-visitor-inventory-items.md) | GET | Retrieves a visitor's inventory items from Topia. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Enter World](actions/enter-world.md) | GET |  |
| [Get Scene](actions/get-scene.md) | GET | Retrieves a scene from Topia. |
| [Get World Data Object](actions/get-world-data-object.md) | GET | Retrieves a world's data object from Topia. |
| [Get World Details](actions/get-world-details.md) | GET | Retrieves details for a specific Topia world. |
| [List Admin Worlds](actions/list-admin-worlds.md) | GET | Retrieves worlds you administer in Topia. |
| [List Interactive Worlds](actions/list-interactive-worlds.md) | GET | Retrieves worlds with active interactive keys in Topia. |
| [List My Scenes](actions/list-my-scenes.md) | GET | Retrieves scenes owned by your Topia account. |
| [List Topia Scenes](actions/list-topia-scenes.md) | GET | Retrieves Topia-provided scenes from the shared library. |
| [List World Scenes](actions/list-world-scenes.md) | GET | Retrieves scenes from a specific Topia world. |
| [List World Scenes With Dropped Assets](actions/list-world-scenes-with-dropped-assets.md) | GET | Retrieves scenes and dropped assets from a Topia world. |
| [List Worlds](actions/list-worlds.md) | GET | Retrieves worlds available to your Topia account. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Visitor](actions/get-visitor.md) | GET | Retrieves a visitor from a Topia world. |
| [Get Visitor Data Object](actions/get-visitor-data-object.md) | GET | Retrieves a visitor's data object from Topia. |
| [List Visitors](actions/list-visitors.md) | GET | Retrieves visitors from a Topia world. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from a Topia world. |

