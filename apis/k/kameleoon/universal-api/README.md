# <img src="https://images.mindcloud.co/apps/icons/kameleoon-icon_1775152950010.png" alt="Kameleoon logo" width="28" height="28"> Kameleoon: Universal API

Kameleoon is an experimentation and personalization platform. This app wraps Kameleoon REST APIs (Automation/Data/Product Recommendation) for account, experiment, and related management operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kameleoon/latest
- **Category:** Marketing
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.kameleoon.com/
- **Vendor API docs:** https://developers.kameleoon.com/apis/automation-api-rest/get-started/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get all accounts](actions/get-all-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-accounts?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create account](actions/create-account.md) | POST |  |
| [Delete account](actions/delete-account.md) | DELETE |  |
| [Get account](actions/get-account.md) | GET |  |
| [Update account](actions/update-account.md) | PUT |  |

### Block

| Action | Method | Description |
| --- | --- | --- |
| [Get all studio recommender blocks](actions/get-all-studio-recommender-blocks.md) | GET |  |

### Data

| Action | Method | Description |
| --- | --- | --- |
| [Get all custom data](actions/get-all-custom-data.md) | GET |  |

### Experiment

| Action | Method | Description |
| --- | --- | --- |
| [Get all experiments](actions/get-all-experiments.md) | GET |  |

### Goal

| Action | Method | Description |
| --- | --- | --- |
| [Get all goals](actions/get-all-goals.md) | GET |  |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Get all images](actions/get-all-images.md) | GET |  |

### Moment

| Action | Method | Description |
| --- | --- | --- |
| [Get all key moments](actions/get-all-key-moments.md) | GET |  |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get all key pages](actions/get-all-key-pages.md) | GET |  |

### Personalization

| Action | Method | Description |
| --- | --- | --- |
| [Get all personalizations](actions/get-all-personalizations.md) | GET |  |

### Referrer

| Action | Method | Description |
| --- | --- | --- |
| [Get all referrers](actions/get-all-referrers.md) | GET |  |

### Rule

| Action | Method | Description |
| --- | --- | --- |
| [Get all targeting rules](actions/get-all-targeting-rules.md) | GET |  |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get all segments](actions/get-all-segments.md) | GET |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Get all sites](actions/get-all-sites.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get all tags](actions/get-all-tags.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get all accounts](actions/get-all-accounts.md) | GET |  |

### Variation

| Action | Method | Description |
| --- | --- | --- |
| [Get all variations](actions/get-all-variations.md) | GET |  |

### Widget

| Action | Method | Description |
| --- | --- | --- |
| [Get all widget studio templates](actions/get-all-widget-studio-templates.md) | GET |  |
| [Get all widget studios](actions/get-all-widget-studios.md) | GET |  |
| [Get all widget templates](actions/get-all-widget-templates.md) | GET |  |

