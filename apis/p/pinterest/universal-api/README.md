# <img src="https://images.mindcloud.co/apps/icons/pinterest-icon_1782394195426.png" alt="Pinterest logo" width="28" height="28"> Pinterest: Universal API

Pinterest is a visual discovery and social commerce platform for creating and managing Pins, boards, media, catalogs, ads, and account analytics through the Pinterest API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pinterest/latest
- **Category:** Marketing / Social Media
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pinterest.com
- **Vendor API docs:** https://developers.pinterest.com/docs/api/v5/introduction/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Boards](actions/list-boards.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/list-boards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Ad Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Ad Account](actions/get-ad-account.md) | GET | Retrieves an ad account from Pinterest. |
| [List Ad Accounts](actions/list-ad-accounts.md) | GET | Retrieves ad accounts from Pinterest. |

### Ad Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from a Pinterest ad account. |

### Ad Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Ad Groups](actions/list-ad-groups.md) | GET | Retrieves ad groups from a Pinterest ad account. |

### Ads

| Action | Method | Description |
| --- | --- | --- |
| [List Ads](actions/list-ads.md) | GET | Retrieves ads from a Pinterest ad account. |

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog Item Batch Status](actions/get-catalog-item-batch-status.md) | GET | Retrieves the status of a Pinterest catalog item batch. |

### Board Section

| Action | Method | Description |
| --- | --- | --- |
| [Create Board Section](actions/create-board-section.md) | POST | Creates a new board section in Pinterest. |
| [Delete Board Section](actions/delete-board-section.md) | DELETE | Deletes an existing board section from Pinterest. |
| [List Board Sections](actions/list-board-sections.md) | GET | Retrieves board sections from a Pinterest board. |
| [Update Board Section](actions/update-board-section.md) | PUT | Updates an existing board section in Pinterest. |

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [Create Board](actions/create-board.md) | POST | Creates a new board in Pinterest. |
| [Delete Board](actions/delete-board.md) | DELETE | Deletes an existing board from Pinterest. |
| [Get Board](actions/get-board.md) | GET | Retrieves a board from Pinterest. |
| [List Boards](actions/list-boards.md) | GET | Retrieves the current user's boards from Pinterest. |
| [Search Boards](actions/search-boards.md) | GET | Finds boards in Pinterest by search query. |
| [Update Board](actions/update-board.md) | PUT | Updates an existing board in Pinterest. |

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [Create Catalog](actions/create-catalog.md) | POST | Creates a new catalog in Pinterest. |
| [List Catalogs](actions/list-catalogs.md) | GET | Retrieves catalogs from Pinterest. |
| [List Product Groups](actions/list-product-groups.md) | GET | Retrieves product groups from a Pinterest catalog. |

### Creative Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Pin](actions/create-pin.md) | POST | Creates a new pin in Pinterest. |
| [Delete Pin](actions/delete-pin.md) | DELETE | Deletes an existing pin from Pinterest. |
| [Get Pin](actions/get-pin.md) | GET | Retrieves a pin from Pinterest. |
| [List Board Pins](actions/list-board-pins.md) | GET | Retrieves pins from a Pinterest board. |
| [List Board Section Pins](actions/list-board-section-pins.md) | GET | Retrieves pins from a Pinterest board section. |
| [List Pins](actions/list-pins.md) | GET | Retrieves the current user's pins from Pinterest. |
| [Save Pin](actions/save-pin.md) | POST | Saves a pin to a Pinterest board or section. |
| [Search Pins](actions/search-pins.md) | GET | Finds pins in Pinterest by search query. |
| [Update Pin](actions/update-pin.md) | PUT | Updates an existing pin in Pinterest. |

### Media Upload

| Action | Method | Description |
| --- | --- | --- |
| [Get Media Upload](actions/get-media-upload.md) | GET | Retrieves media upload details from Pinterest. |
| [Register Media Upload](actions/register-media-upload.md) | POST | Registers a media upload with Pinterest. |

### Pin Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Top Pins Analytics](actions/get-top-pins-analytics.md) | GET | Retrieves top pin analytics from Pinterest. |
| [Get Top Video Pins Analytics](actions/get-top-video-pins-analytics.md) | GET | Retrieves top video pin analytics from Pinterest. |

### Pinterest Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get User Account Analytics](actions/get-user-account-analytics.md) | GET | Retrieves analytics for the current Pinterest user account. |

### Product Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Group](actions/get-product-group.md) | GET | Retrieves a product group from a Pinterest catalog. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog Items](actions/get-catalog-items.md) | GET | Retrieves catalog items from Pinterest. |
| [List Products By Product Group](actions/list-products-by-product-group.md) | GET | Retrieves product pins from a Pinterest product group. |
| [Operate On Product Pins](actions/operate-on-product-pins.md) | PUT | Operates on Pinterest catalog items in batch. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get User Account](actions/get-user-account.md) | GET | Retrieves the current user account from Pinterest. |
| [List Followers](actions/list-followers.md) | GET | Retrieves the current user's followers from Pinterest. |

