# <img src="https://images.mindcloud.co/apps/icons/nifty-images_1774637169241.png" alt="NiftyImages logo" width="28" height="28"> NiftyImages: Universal API

Create personalized images, countdown timers, maps, and real-time email marketing visuals with the NiftyImages API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/niftyImages/latest
- **Category:** Marketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://niftyimages.com
- **Vendor API docs:** https://api.niftyimages.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Widgets](actions/list-widgets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-widgets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Bee Plugin User

| Action | Method | Description |
| --- | --- | --- |
| [List Bee Plugin Users](actions/list-bee-plugin-users.md) | GET | Retrieves Bee Plugin users from NiftyImages. |
| [Set Bee Plugin User Suspended](actions/set-bee-plugin-user-suspended.md) | PUT | Updates a Bee Plugin user suspension in NiftyImages. |

### Bee Plugin User Image

| Action | Method | Description |
| --- | --- | --- |
| [List Bee Plugin User Images](actions/list-bee-plugin-user-images.md) | GET | Retrieves Bee Plugin user images from NiftyImages. |

### Chatfuel Response

| Action | Method | Description |
| --- | --- | --- |
| [Create ChatFuel Response Image](actions/create-chat-fuel-response-image.md) | POST | Creates a ChatFuel response image in NiftyImages. |

### Data Store Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Store Fields](actions/list-store-fields.md) | GET | Retrieves data store fields from NiftyImages. |

### Data Store Record

| Action | Method | Description |
| --- | --- | --- |
| [Delete Store Record By ID](actions/delete-store-record-by-id.md) | DELETE | Deletes a data store record from NiftyImages by record ID. |
| [Delete Store Record By Payload](actions/delete-store-record-by-payload.md) | DELETE | Deletes a data store record from NiftyImages by payload. |
| [Upsert Store Record](actions/upsert-store-record.md) | PUT | Updates or creates a data store record in NiftyImages. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Delete Image](actions/delete-image.md) | DELETE | Deletes an image from NiftyImages. |
| [Get Image Details](actions/get-image-details.md) | GET | Retrieves image details from NiftyImages. |
| [List Images](actions/list-images.md) | GET | Retrieves images from NiftyImages. |

### Image Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Aggregated Image Stats](actions/get-image-stats.md) | GET | Retrieves aggregated image stats from NiftyImages. |

### Manychat Response

| Action | Method | Description |
| --- | --- | --- |
| [Create ManyChat Response Image](actions/create-many-chat-response-image.md) | POST | Creates a ManyChat response image in NiftyImages. |

### Map

| Action | Method | Description |
| --- | --- | --- |
| [Get Map Details](actions/get-map-details.md) | GET | Retrieves map details from NiftyImages. |
| [List Maps](actions/list-maps.md) | GET | Retrieves maps from NiftyImages. |

### Map Location

| Action | Method | Description |
| --- | --- | --- |
| [Add Map Location](actions/add-map-location.md) | POST | Creates a new map location in NiftyImages. |
| [Delete Map Location By Location ID](actions/delete-map-location-by-location-id.md) | DELETE | Deletes a map location from NiftyImages by location ID. |
| [Delete Map Location By Nifty ID](actions/delete-map-location-by-nifty-id.md) | DELETE | Deletes a map location from NiftyImages by Nifty ID. |
| [Search Map Locations By Address](actions/search-map-locations-by-address.md) | GET | Finds map locations in NiftyImages by address. |
| [Search Map Locations By Coordinates](actions/search-map-locations-by-coordinates.md) | GET | Finds map locations in NiftyImages by coordinates. |
| [Search Map Locations By Location ID](actions/search-map-locations-by-location-id.md) | GET | Finds map locations in NiftyImages by location ID. |
| [Search Map Locations By Nifty ID](actions/search-map-locations-by-nifty-id.md) | GET | Finds map locations in NiftyImages by Nifty ID. |
| [Update Map Location](actions/update-map-location.md) | PUT | Updates an existing map location in NiftyImages. |

### Personalized Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Personalized Image Details](actions/get-personalized-image-details.md) | GET | Retrieves personalized image details from NiftyImages. |
| [Update Personalized Image Font Color](actions/update-personalized-image-font-color.md) | PUT | Updates personalized image font color in NiftyImages. |
| [Update Personalized Image Text](actions/update-personalized-image-text.md) | PUT | Updates personalized image text in NiftyImages. |

### Photoshop Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Photoshop Image Details](actions/get-photoshop-image-details.md) | GET | Retrieves Photoshop image details from NiftyImages. |
| [Update Photoshop Image Layers](actions/update-photoshop-image-layers.md) | PUT | Updates Photoshop image layers in NiftyImages. |
| [Update Photoshop Layer Visibility](actions/update-photoshop-layer-visibility.md) | PUT | Updates Photoshop layer visibility in NiftyImages. |
| [Update Photoshop Shape Color](actions/update-photoshop-shape-color.md) | PUT | Updates a Photoshop shape color in NiftyImages. |
| [Update Photoshop Smart Object Image](actions/update-photoshop-smart-object-image.md) | PUT | Updates a Photoshop smart object image in NiftyImages. |
| [Update Photoshop Text Layer](actions/update-photoshop-text-layer.md) | PUT | Updates a Photoshop text layer in NiftyImages. |

### Timer

| Action | Method | Description |
| --- | --- | --- |
| [Update Timer Target Date](actions/update-timer-target-date.md) | PUT | Updates a timer target date in NiftyImages. |

### Widget

| Action | Method | Description |
| --- | --- | --- |
| [List Widgets](actions/list-widgets.md) | GET | Retrieves widgets from NiftyImages. |

### Widget Image

| Action | Method | Description |
| --- | --- | --- |
| [List Widget Images](actions/list-widget-images.md) | GET | Retrieves widget images from NiftyImages. |

### Widget Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Widget Stats Summary](actions/get-widget-stats-summary.md) | GET | Retrieves widget stats summary from NiftyImages. |

### Widget User

| Action | Method | Description |
| --- | --- | --- |
| [List Widget Users](actions/list-widget-users.md) | GET | Retrieves widget users from NiftyImages. |
| [Set Widget User Suspended](actions/set-widget-user-suspended.md) | PUT | Updates a widget user suspension in NiftyImages. |

### Widget User Image

| Action | Method | Description |
| --- | --- | --- |
| [List Widget User Images](actions/list-widget-user-images.md) | GET | Retrieves widget user images from NiftyImages. |

### Widget User Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Widget User Stats](actions/get-widget-user-stats.md) | GET | Retrieves widget user stats from NiftyImages. |

