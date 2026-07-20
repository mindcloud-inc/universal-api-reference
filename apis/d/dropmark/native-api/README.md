# Dropmark: Native API Reference

A consolidated summary of Dropmark's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://support.dropmark.com/article/96-api
- **API base URL:** `https://{subdomain}`

## Authentication

### Feed API Key

Use a Dropmark dashboard subdomain and activity feed key to access the activity feed. Collection endpoints require a collection-specific key or basic auth.

### Credentials

- **Subdomain:** `subdomain` · required · The full Dropmark dashboard host, for example `mindcloudapps.dropmark.com`.
- **Activity Feed Key:** `activityKey` · required · Personal read-only Dropmark activity feed key from Account > Private links > Activity feed. Dropmark documents these keys as endpoint-specific, so this value is only used for activity requests.

[Official authentication documentation](https://support.dropmark.com/article/96-api)

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | `GET /activity.json` | [docs](https://support.dropmark.com/article/96-api) |
| [Get Activity Feed](actions/get-activity-feed.md) | `GET /activity.{{args.format}}` | [docs](https://support.dropmark.com/article/96-api) |
| [Get Activity RSS](actions/get-activity-rss.md) | `GET /activity.rss` | [docs](https://support.dropmark.com/article/96-api) |
| [Get Activity XML](actions/get-activity-xml.md) | `GET /activity.xml` | [docs](https://support.dropmark.com/article/96-api) |
| [Get Collection](actions/get-collection.md) | `GET /{{args.collectionId}}.json` | [docs](https://support.dropmark.com/article/96-api) |
| [Get Collection CSV](actions/get-collection-csv.md) | `GET /{{args.collectionId}}.csv` | [docs](https://support.dropmark.com/article/96-api) |
| [Get Collection Export](actions/get-collection-export.md) | `GET /{{args.collectionId}}.{{args.format}}` | [docs](https://support.dropmark.com/article/96-api) |
| [Get Collection PLS](actions/get-collection-pls.md) | `GET /{{args.collectionId}}.pls` | [docs](https://support.dropmark.com/article/96-api) |
| [Get Collection RSS](actions/get-collection-rss.md) | `GET /{{args.collectionId}}.rss` | [docs](https://support.dropmark.com/article/96-api) |
| [Get Collection XML](actions/get-collection-xml.md) | `GET /{{args.collectionId}}.xml` | [docs](https://support.dropmark.com/article/96-api) |
