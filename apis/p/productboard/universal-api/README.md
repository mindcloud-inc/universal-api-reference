# <img src="https://images.mindcloud.co/apps/icons/productboard_1773276788647.png" alt="Productboard logo" width="28" height="28"> Productboard: Universal API

Manage features, products, releases, objectives, and components

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/productboard/latest
- **Category:** Productivity / Project Management
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.productboard.com
- **Vendor API docs:** https://developer.productboard.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List All Features](actions/list-all-features.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productboard/latest/actions/list-all-features?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Component

| Action | Method | Description |
| --- | --- | --- |
| [Get Component](actions/get-component.md) | GET | Retrieves a component from your Productboard workspace. |
| [List All Components](actions/list-all-components.md) | GET | Retrieves components from your Productboard workspace. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields by Type](actions/list-custom-fields-by-type.md) | GET | Retrieves custom fields for a Productboard hierarchy type. |

### Feature

| Action | Method | Description |
| --- | --- | --- |
| [Get Feature](actions/get-feature.md) | GET | Retrieves a feature from your Productboard workspace. |
| [List All Features](actions/list-all-features.md) | GET | Retrieves features from your Productboard workspace. |

### Feature Status

| Action | Method | Description |
| --- | --- | --- |
| [List All Feature Statuses](actions/list-all-feature-statuses.md) | GET | Retrieves feature statuses from your Productboard workspace. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [List All Notes](actions/list-all-notes.md) | GET | Retrieves notes from your Productboard workspace. |

### Objectives

| Action | Method | Description |
| --- | --- | --- |
| [Get Objective](actions/get-objective.md) | GET | Retrieves an objective from your Productboard workspace. |
| [List All Objectives](actions/list-all-objectives.md) | GET | Retrieves objectives from your Productboard workspace. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from your Productboard workspace. |
| [List All Products](actions/list-all-products.md) | GET | Retrieves products from your Productboard workspace. |

### Releases

| Action | Method | Description |
| --- | --- | --- |
| [Get Release](actions/get-release.md) | GET | Retrieves a release from your Productboard workspace. |
| [List All Releases](actions/list-all-releases.md) | GET | Retrieves releases from your Productboard workspace. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List All Users](actions/list-all-users.md) | GET | Retrieves users from your Productboard workspace. |

