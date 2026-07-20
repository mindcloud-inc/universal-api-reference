# <img src="https://images.mindcloud.co/apps/icons/web-change-detector_1774895514891.png" alt="WebChange Detector logo" width="28" height="28"> WebChange Detector: Universal API

Monitor websites for visual changes, compare screenshots, manage groups and URLs, and receive alerts and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webChangeDetector/latest
- **Category:** IT Operations / Observability
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.webchangedetector.com/
- **Vendor API docs:** https://api.webchangedetector.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webChangeDetector/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Add URLs To Group](actions/add-urls-to-group.md) | PUT | Adds URLs to a group in WebChange Detector. |
| [Create Group](actions/create-group.md) | POST | Creates a new group in WebChange Detector. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from WebChange Detector. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from WebChange Detector. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from WebChange Detector. |
| [Remove URLs From Group](actions/remove-urls-from-group.md) | PUT | Removes URLs from a group in WebChange Detector. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in WebChange Detector. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Create URL](actions/create-url.md) | POST | Creates a new URL in WebChange Detector. |
| [Delete URL](actions/delete-url.md) | DELETE | Deletes an existing URL from WebChange Detector. |
| [Get URL](actions/get-url.md) | GET | Retrieves a URL from WebChange Detector. |
| [List Group URLs](actions/list-group-urls.md) | GET | Retrieves URLs for a group from WebChange Detector. |
| [List URLs](actions/list-urls.md) | GET | Retrieves URLs from WebChange Detector. |
| [Update URL](actions/update-url.md) | PUT | Updates an existing URL in WebChange Detector. |

### Service Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from WebChange Detector. |
| [Get Account Stats](actions/get-account-stats.md) | GET | Retrieves aggregated account statistics from WebChange Detector. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in WebChange Detector. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from WebChange Detector. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from WebChange Detector. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from WebChange Detector. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in WebChange Detector. |

