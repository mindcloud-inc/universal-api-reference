# NiftyImages: Native API Reference

A consolidated summary of NiftyImages's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api.niftyimages.com/
- **API base URL:** `https://api.niftyimages.com/v1`

## Authentication

### API Key

Connect NiftyImages with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.niftyimages.com/)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Map Location](actions/add-map-location.md) | `POST /Maps/AddLocation` | [docs](https://api.niftyimages.com/) |
| [Create ChatFuel Response Image](actions/create-chat-fuel-response-image.md) | `POST /ChatFuel` | [docs](https://api.niftyimages.com/) |
| [Create ManyChat Response Image](actions/create-many-chat-response-image.md) | `POST /ManyChat` | [docs](https://api.niftyimages.com/) |
| [Delete Image](actions/delete-image.md) | `DELETE /Image` | [docs](https://api.niftyimages.com/) |
| [Delete Map Location By Location ID](actions/delete-map-location-by-location-id.md) | `DELETE /Maps/DeleteLocation` | [docs](https://api.niftyimages.com/) |
| [Delete Map Location By Nifty ID](actions/delete-map-location-by-nifty-id.md) | `DELETE /Maps/DeleteLocation` | [docs](https://api.niftyimages.com/) |
| [Delete Store Record By ID](actions/delete-store-record-by-id.md) | `DELETE /Store/DeleteID` | [docs](https://api.niftyimages.com/) |
| [Delete Store Record By Payload](actions/delete-store-record-by-payload.md) | `DELETE /Store/DeleteRecord` | [docs](https://api.niftyimages.com/) |
| [Get Image Details](actions/get-image-details.md) | `GET /Image` | [docs](https://api.niftyimages.com/) |
| [Get Aggregated Image Stats](actions/get-image-stats.md) | `GET /Images/AllStats` | [docs](https://api.niftyimages.com/) |
| [Get Map Details](actions/get-map-details.md) | `GET /Maps/Details` | [docs](https://api.niftyimages.com/) |
| [Get Personalized Image Details](actions/get-personalized-image-details.md) | `GET /Personalized` | [docs](https://api.niftyimages.com/) |
| [Get Photoshop Image Details](actions/get-photoshop-image-details.md) | `GET /Psd` | [docs](https://api.niftyimages.com/) |
| [Get Widget Stats Summary](actions/get-widget-stats-summary.md) | `GET /Widgets/AllStats` | [docs](https://api.niftyimages.com/) |
| [Get Widget User Stats](actions/get-widget-user-stats.md) | `GET /Widgets/:widgetKey/Users/:user` | [docs](https://api.niftyimages.com/) |
| [List Bee Plugin User Images](actions/list-bee-plugin-user-images.md) | `GET /BeePlugin/:pluginKey/Users/:user` | [docs](https://api.niftyimages.com/) |
| [List Bee Plugin Users](actions/list-bee-plugin-users.md) | `GET /BeePlugin/:pluginKey/Users` | [docs](https://api.niftyimages.com/) |
| [List Images](actions/list-images.md) | `GET /Images` | [docs](https://api.niftyimages.com/) |
| [List Maps](actions/list-maps.md) | `GET /Maps` | [docs](https://api.niftyimages.com/) |
| [Get Store Fields](actions/list-store-fields.md) | `GET /Store` | [docs](https://api.niftyimages.com/) |
| [List Widget Images](actions/list-widget-images.md) | `GET /Widgets/:widgetKey/Images` | [docs](https://api.niftyimages.com/) |
| [List Widget User Images](actions/list-widget-user-images.md) | `GET /Widgets/:widgetKey/Images/:user` | [docs](https://api.niftyimages.com/) |
| [List Widget Users](actions/list-widget-users.md) | `GET /Widgets/:widgetKey/Users` | [docs](https://api.niftyimages.com/) |
| [List Widgets](actions/list-widgets.md) | `GET /Widgets` | [docs](https://api.niftyimages.com/) |
| [Search Map Locations By Address](actions/search-map-locations-by-address.md) | `GET /Maps/GetLocations` | [docs](https://api.niftyimages.com/) |
| [Search Map Locations By Coordinates](actions/search-map-locations-by-coordinates.md) | `GET /Maps/GetLocations` | [docs](https://api.niftyimages.com/) |
| [Search Map Locations By Location ID](actions/search-map-locations-by-location-id.md) | `GET /Maps/GetLocations` | [docs](https://api.niftyimages.com/) |
| [Search Map Locations By Nifty ID](actions/search-map-locations-by-nifty-id.md) | `GET /Maps/GetLocations` | [docs](https://api.niftyimages.com/) |
| [Set Bee Plugin User Suspended](actions/set-bee-plugin-user-suspended.md) | `PUT /BeePlugin/:pluginKey/Users/:user` | [docs](https://api.niftyimages.com/) |
| [Set Widget User Suspended](actions/set-widget-user-suspended.md) | `PUT /Widgets/:widgetKey/Users/:user` | [docs](https://api.niftyimages.com/) |
| [Update Map Location](actions/update-map-location.md) | `PUT /Maps/UpdateLocation` | [docs](https://api.niftyimages.com/) |
| [Update Personalized Image Font Color](actions/update-personalized-image-font-color.md) | `PUT /Personalized` | [docs](https://api.niftyimages.com/) |
| [Update Personalized Image Text](actions/update-personalized-image-text.md) | `PUT /Personalized` | [docs](https://api.niftyimages.com/) |
| [Update Photoshop Image Layers](actions/update-photoshop-image-layers.md) | `PUT /Psd` | [docs](https://api.niftyimages.com/) |
| [Update Photoshop Layer Visibility](actions/update-photoshop-layer-visibility.md) | `PUT /Psd` | [docs](https://api.niftyimages.com/) |
| [Update Photoshop Shape Color](actions/update-photoshop-shape-color.md) | `PUT /Psd` | [docs](https://api.niftyimages.com/) |
| [Update Photoshop Smart Object Image](actions/update-photoshop-smart-object-image.md) | `PUT /Psd` | [docs](https://api.niftyimages.com/) |
| [Update Photoshop Text Layer](actions/update-photoshop-text-layer.md) | `PUT /Psd` | [docs](https://api.niftyimages.com/) |
| [Update Timer Target Date](actions/update-timer-target-date.md) | `PUT /Timer/Update` | [docs](https://api.niftyimages.com/) |
| [Upsert Store Record](actions/upsert-store-record.md) | `POST /Store/AddRecord` | [docs](https://api.niftyimages.com/) |
