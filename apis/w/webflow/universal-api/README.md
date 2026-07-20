# <img src="https://images.mindcloud.co/apps/icons/webflow_1772739950672.png" alt="Webflow logo" width="28" height="28"> Webflow: Universal API

Design websites, manage CMS content, publish pages, and optimize SEO.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webflow/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://webflow.com
- **Vendor API docs:** https://developers.webflow.com/data/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Webflow. |
| [Get Collection Details](actions/get-collection-details.md) | GET | Retrieves details for a collection from Webflow. |
| [List Collections](actions/list-collections.md) | GET | Retrieves a list of collections from Webflow. |

### Component

| Action | Method | Description |
| --- | --- | --- |
| [Get Component Content](actions/get-component-content.md) | GET | Retrieves content for a component from Webflow. |
| [Get Component Properties](actions/get-component-properties.md) | GET | Retrieves properties for a component from Webflow. |
| [List Components](actions/list-components.md) | GET | Retrieves a list of components from Webflow. |
| [Update Component Content](actions/update-component-content.md) | PUT | Updates content for a component in Webflow. |
| [Update Component Properties](actions/update-component-properties.md) | PUT | Updates properties for a component in Webflow. |

### Custom Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Domains](actions/list-custom-domains.md) | GET | Retrieves custom domains for a site from Webflow. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Items](actions/create-items.md) | POST | Creates staged collection items in Webflow. |
| [Get Item](actions/get-item.md) | GET | Retrieves a staged collection item from Webflow. |
| [List Items](actions/list-items.md) | GET | Retrieves staged collection items from Webflow. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Content](actions/get-page-content.md) | GET | Retrieves static page content from Webflow. |
| [Get Page Metadata](actions/get-page-metadata.md) | GET | Retrieves metadata for a page from Webflow. |
| [List Pages](actions/list-pages.md) | GET | Retrieves a list of pages from Webflow. |
| [Update Page Content](actions/update-page-content.md) | PUT | Updates static page content in Webflow. |
| [Update Page Metadata](actions/update-page-metadata.md) | PUT | Updates metadata for a page in Webflow. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Get Site](actions/get-site.md) | GET | Retrieves a site from Webflow. |
| [List Sites](actions/list-sites.md) | GET | Retrieves a list of sites from Webflow. |
| [Publish Site](actions/publish-site.md) | PUT | Publishes a site in Webflow. |

