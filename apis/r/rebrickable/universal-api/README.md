# <img src="https://images.mindcloud.co/apps/icons/bot1_1777488970013.png" alt="Rebrickable logo" width="28" height="28"> Rebrickable: Universal API

Access Rebrickable's LEGO catalog data for sets, parts, colors, themes, minifigs, badges, and related inventory lookups through the Rebrickable API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rebrickable/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rebrickable.com/
- **Vendor API docs:** https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Colors](actions/list-colors.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-colors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Alternate Build

| Action | Method | Description |
| --- | --- | --- |
| [List Alternate Builds for Set](actions/list-alternate-builds-for-set.md) | GET | Retrieves alternate builds for a LEGO set in Rebrickable. |

### Badge

| Action | Method | Description |
| --- | --- | --- |
| [Get Badge](actions/get-badge.md) | GET | Retrieves a badge from Rebrickable by ID. |
| [List Badges](actions/list-badges.md) | GET | Retrieves badges from Rebrickable user profiles. |

### Color

| Action | Method | Description |
| --- | --- | --- |
| [Get Color](actions/get-color.md) | GET | Retrieves a LEGO color from Rebrickable by ID. |
| [List Colors](actions/list-colors.md) | GET | Retrieves LEGO color records from Rebrickable. |

### Element

| Action | Method | Description |
| --- | --- | --- |
| [Get Element](actions/get-element.md) | GET | Retrieves a LEGO element from Rebrickable by element ID. |

### Inventory Part

| Action | Method | Description |
| --- | --- | --- |
| [List Minifig Parts](actions/list-minifig-parts.md) | GET | Retrieves parts for a LEGO minifig in Rebrickable. |
| [List Set Parts](actions/list-set-parts.md) | GET | Retrieves parts for a LEGO set in Rebrickable. |

### Minifig

| Action | Method | Description |
| --- | --- | --- |
| [Get Minifig](actions/get-minifig.md) | GET | Retrieves a LEGO minifig from Rebrickable by set number. |
| [List Minifigs](actions/list-minifigs.md) | GET | Finds LEGO minifig records in Rebrickable. |
| [List Set Minifigs](actions/list-set-minifigs.md) | GET | Retrieves minifigs for a LEGO set in Rebrickable. |

### Part

| Action | Method | Description |
| --- | --- | --- |
| [Get Part](actions/get-part.md) | GET | Retrieves a LEGO part from Rebrickable by part number. |
| [List Parts](actions/list-parts.md) | GET | Finds LEGO part records in Rebrickable. |

### Part Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Part Category](actions/get-part-category.md) | GET | Retrieves a LEGO part category from Rebrickable by ID. |
| [List Part Categories](actions/list-part-categories.md) | GET | Retrieves LEGO part categories from Rebrickable. |

### Part Color

| Action | Method | Description |
| --- | --- | --- |
| [Get Part Color](actions/get-part-color.md) | GET | Retrieves a LEGO part color from Rebrickable. |
| [List Part Colors](actions/list-part-colors.md) | GET | Retrieves available colors for a LEGO part in Rebrickable. |

### Set

| Action | Method | Description |
| --- | --- | --- |
| [Get Set](actions/get-set.md) | GET | Retrieves a LEGO set from Rebrickable by set number. |
| [List Set Subsets](actions/list-set-subsets.md) | GET | Retrieves subsets for a LEGO set in Rebrickable. |
| [List Sets](actions/list-sets.md) | GET | Finds LEGO set records in Rebrickable. |
| [List Sets Containing Minifig](actions/list-sets-containing-minifig.md) | GET | Retrieves sets containing a LEGO minifig in Rebrickable. |
| [List Sets Containing Part Color](actions/list-sets-containing-part-color.md) | GET | Retrieves sets containing a LEGO part color in Rebrickable. |

### Theme

| Action | Method | Description |
| --- | --- | --- |
| [Get Theme](actions/get-theme.md) | GET | Retrieves a LEGO theme from Rebrickable by ID. |
| [List Themes](actions/list-themes.md) | GET | Retrieves LEGO theme records from Rebrickable. |

