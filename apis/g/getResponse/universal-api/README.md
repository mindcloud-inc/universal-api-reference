# <img src="https://images.mindcloud.co/apps/icons/get-response_1773081409518.png" alt="GetResponse logo" width="28" height="28"> GetResponse: Universal API

GetResponse: Manage contacts, campaigns, newsletters, and marketing automation workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/getResponse/latest
- **Category:** Marketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.getresponse.com
- **Vendor API docs:** https://apireference.getresponse.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves your current GetResponse account details. |

### Address

| Action | Method | Description |
| --- | --- | --- |
| [List Addresses](actions/list-addresses.md) | GET | Retrieves a list of addresses from GetResponse. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves a list of campaigns from GetResponse. |

### Campaignstatistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Statistics Balance](actions/get-campaign-statistics-balance.md) | GET | Retrieves balance statistics for GetResponse campaigns. |
| [Get Campaign Statistics List Size](actions/get-campaign-statistics-list-size.md) | GET | Retrieves list size statistics for GetResponse campaigns. |
| [Get Campaign Statistics Locations](actions/get-campaign-statistics-locations.md) | GET | Retrieves subscriber location statistics for GetResponse campaigns. |
| [Get Campaign Statistics Origins](actions/get-campaign-statistics-origins.md) | GET | Retrieves subscriber origin statistics for GetResponse campaigns. |
| [Get Campaign Statistics Removals](actions/get-campaign-statistics-removals.md) | GET | Retrieves removal statistics for GetResponse campaigns. |
| [Get Campaign Statistics Subscriptions](actions/get-campaign-statistics-subscriptions.md) | GET | Retrieves subscription counts and origins for GetResponse campaigns. |
| [Get Campaign Statistics Summary](actions/get-campaign-statistics-summary.md) | GET | Retrieves summary statistics for selected GetResponse campaigns. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in GetResponse. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact by ID from GetResponse. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves contact details by ID from GetResponse. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from GetResponse. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in GetResponse. |

### Customfield

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves a list of custom fields from GetResponse. |

### Facebookpixel

| Action | Method | Description |
| --- | --- | --- |
| [List Facebook Pixels](actions/list-facebook-pixels.md) | GET | Retrieves a list of Facebook pixels from GetResponse. |

### Fromfield

| Action | Method | Description |
| --- | --- | --- |
| [List From Fields](actions/list-from-fields.md) | GET | Retrieves From addresses from GetResponse. |

### Industry

| Action | Method | Description |
| --- | --- | --- |
| [List Industries](actions/list-industries.md) | GET | Retrieves available industry tags from GetResponse. |

### Loginhistory

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Login History](actions/get-account-login-history.md) | GET | Retrieves login history for your GetResponse account. |

### Newsletter

| Action | Method | Description |
| --- | --- | --- |
| [List Newsletters](actions/list-newsletters.md) | GET | Retrieves a list of newsletters from GetResponse. |

### Newsletterstatistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Newsletter Statistics](actions/get-newsletter-statistics.md) | GET | Retrieves total newsletter statistics from GetResponse. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in a GetResponse shop. |
| [Create Shop](actions/create-shop.md) | POST | Creates a new shop in GetResponse. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from a GetResponse shop. |
| [Delete Shop](actions/delete-shop.md) | DELETE | Deletes an existing shop from GetResponse. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product by ID from a GetResponse shop. |
| [Get Shop](actions/get-shop.md) | GET | Retrieves a shop by ID from GetResponse. |
| [List Products](actions/list-products.md) | GET | Retrieves products from a GetResponse shop. |
| [List Shops](actions/list-shops.md) | GET | Retrieves a list of shops from GetResponse. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in a GetResponse shop. |
| [Update Shop](actions/update-shop.md) | PUT | Updates an existing shop in GetResponse. |
| [Upsert Product Categories](actions/upsert-product-categories.md) | PUT | Creates or updates product categories for a GetResponse shop product. |
| [Upsert Product Meta Fields](actions/upsert-product-meta-fields.md) | PUT | Creates or updates product meta fields for a GetResponse shop product. |

### Searchcontact

| Action | Method | Description |
| --- | --- | --- |
| [List Search Contacts](actions/list-search-contacts.md) | GET | Retrieves saved search contact lists from GetResponse. |

### Sendinglimit

| Action | Method | Description |
| --- | --- | --- |
| [Get Sending Limits](actions/get-sending-limits.md) | GET | Retrieves current sending limits from GetResponse. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves a list of tags from GetResponse. |

### Timezone

| Action | Method | Description |
| --- | --- | --- |
| [List Timezones](actions/list-timezones.md) | GET | Retrieves the list of available GetResponse timezones. |

### Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Get Tracking Snippets](actions/get-tracking-snippets.md) | GET | Retrieves tracking code snippets from GetResponse. |

### Website

| Action | Method | Description |
| --- | --- | --- |
| [List Websites](actions/list-websites.md) | GET | Retrieves a list of websites from GetResponse. |

