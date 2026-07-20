# Crazy Egg: Native API Reference

A consolidated summary of Crazy Egg's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://support.crazyegg.com/knowledge-base/
- **API base URL:** `https://app.crazyegg.com/api/v2`

## Authentication

### Crazy Egg Credentials

Snapshot Management API key, Snapshot Management API secret, and Conversion Tracking API key.

### Credentials

- **Snapshot Management API Key:** `apiKey` · required
- **Snapshot Management API Secret:** `secret` · required
- **Conversion Tracking API Key:** `conversionTrackingApiKey` · required

[Official authentication documentation](https://core.crazyegg.com/options/site-settings/475693/api?site=mindcloud.co&siteId=475693)

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate API Signature](actions/authenticate-api-signature.md) | `GET /authenticate.json` | [docs](https://support.crazyegg.com/knowledge-base/) |
| [Check API Status](actions/check-api-status.md) | `GET /status.json` | [docs](https://support.crazyegg.com/knowledge-base/) |
| [Create Snapshot](actions/create-snapshot.md) | `POST /snapshots.json` | [docs](https://support.crazyegg.com/knowledge-base/) |
| [Get Snapshot](actions/get-snapshot.md) | `GET /snapshot/:id.json` | [docs](https://support.crazyegg.com/knowledge-base/) |
| [List Snapshots](actions/list-snapshots.md) | `GET /snapshots.json` | [docs](https://support.crazyegg.com/knowledge-base/) |
| [Restart Snapshot](actions/restart-snapshot.md) | `PUT /snapshot/:id/restart.json` | [docs](https://support.crazyegg.com/knowledge-base/) |
| [Stop Snapshot](actions/stop-snapshot.md) | `PUT /snapshot/:id/stop.json` | [docs](https://support.crazyegg.com/knowledge-base/) |
| [Track Conversion](actions/track-conversion.md) | `POST https://track.crazyegg.com/api/v1` | [docs](https://support.crazyegg.com/knowledge-base/conversion-tracking-api/) |
| [Update Snapshot](actions/update-snapshot.md) | `PUT /snapshot/:id.json` | [docs](https://support.crazyegg.com/knowledge-base/) |
