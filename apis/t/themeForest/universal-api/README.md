# <img src="https://images.mindcloud.co/apps/icons/24438-themeforest-logo-envato-icon-vector-icon-vector-eps_1777392283943.png" alt="Themeforest logo" width="28" height="28"> Themeforest: Universal API

Search ThemeForest marketplace items, inspect Envato catalog details, and access connected Envato Market account, purchase, and author-sale data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/themeForest/latest
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://themeforest.net
- **Vendor API docs:** https://build.envato.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Email](actions/get-account-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-account-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Catalog Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog Collection](actions/get-catalog-collection.md) | GET | Retrieves details for an Envato catalog collection. |

### Catalog Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog Item](actions/get-catalog-item.md) | GET | Retrieves details for an Envato catalog item. |

### Catalog Item Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog Item Version](actions/get-catalog-item-version.md) | GET | Retrieves the latest version for an Envato catalog item. |

### Envato Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves details for the connected Envato account. |

### Envato Account Email

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Email](actions/get-account-email.md) | GET | Retrieves the connected Envato account email. |

### Envato Author Sale

| Action | Method | Description |
| --- | --- | --- |
| [List Author Sales](actions/list-author-sales.md) | GET | Retrieves author sales from Envato Market. |

### Envato Purchase

| Action | Method | Description |
| --- | --- | --- |
| [List Purchases](actions/list-purchases.md) | GET | Retrieves Envato purchases for the connected account. |

### Envato User Badge

| Action | Method | Description |
| --- | --- | --- |
| [Get User Badges](actions/get-user-badges.md) | GET | Retrieves badges for an Envato user. |

### Envato User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves profile details for an Envato user. |

### Envato Username

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Username](actions/get-account-username.md) | GET | Retrieves the connected Envato account username. |

### Featured Themeforest Item

| Action | Method | Description |
| --- | --- | --- |
| [Get ThemeForest Featured Items](actions/get-themeforest-featured-items.md) | GET | Retrieves featured marketplace items from ThemeForest. |

### Item Comment

| Action | Method | Description |
| --- | --- | --- |
| [Search Item Comments](actions/search-item-comments.md) | GET | Finds comments for an Envato item by search term. |

### Item Price

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Prices](actions/get-item-prices.md) | GET | Retrieves license prices for an Envato item. |

### New Themeforest File

| Action | Method | Description |
| --- | --- | --- |
| [Get ThemeForest New Files](actions/get-themeforest-new-files.md) | GET | Retrieves new marketplace files for a ThemeForest category. |

### Popular Themeforest Item

| Action | Method | Description |
| --- | --- | --- |
| [Get ThemeForest Popular Items](actions/get-themeforest-popular-items.md) | GET | Retrieves popular marketplace items from ThemeForest. |

### Random New Themeforest File

| Action | Method | Description |
| --- | --- | --- |
| [Get ThemeForest Random New Files](actions/get-themeforest-random-new-files.md) | GET | Retrieves random new marketplace files from ThemeForest. |

### Similar Item

| Action | Method | Description |
| --- | --- | --- |
| [Find Similar Items](actions/find-similar-items.md) | GET | Finds items similar to an Envato item. |

### Themeforest Category

| Action | Method | Description |
| --- | --- | --- |
| [Get ThemeForest Categories](actions/get-themeforest-categories.md) | GET | Retrieves marketplace category listings from ThemeForest. |

### Themeforest File Count

| Action | Method | Description |
| --- | --- | --- |
| [Get ThemeForest File Counts](actions/get-themeforest-file-counts.md) | GET | Retrieves marketplace file counts from ThemeForest. |

### Themeforest Item

| Action | Method | Description |
| --- | --- | --- |
| [Search ThemeForest Items](actions/search-themeforest-items.md) | GET | Finds ThemeForest items by search term. |

### User Item By Site

| Action | Method | Description |
| --- | --- | --- |
| [Get User Items By Site](actions/get-user-items-by-site.md) | GET | Retrieves an Envato user's item counts by site. |

### User New File

| Action | Method | Description |
| --- | --- | --- |
| [Get New Files From User](actions/get-new-files-from-user.md) | GET | Retrieves new marketplace files from an Envato user. |

