# Nightfall.ai: Native API Reference

A consolidated summary of Nightfall.ai's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://help.nightfall.ai/developer-api
- **API base URL:** `https://api.nightfall.ai`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.nightfall.ai/developer-api/introduction/authentication_security)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextPageToken`.

## Pagination

Use `limit` in the query string to set the page size. Use `pageToken` in the query string as the pagination cursor; numbering starts at 0.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Annotate Finding](actions/annotate-finding.md) | `POST /dlp/v1/findings/:findingId/annotate` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/saas) |
| [Create File Upload](actions/create-file-upload.md) | `POST /v3/upload` | [docs](https://help.nightfall.ai/developer-api/key-concepts/file_scan/scan_api_calls) |
| [Finish File Upload](actions/finish-file-upload.md) | `POST /v3/upload/:fileId/finish` | [docs](https://help.nightfall.ai/developer-api/key-concepts/file_scan/scan_api_calls) |
| [Get Annotation](actions/get-annotation.md) | `GET /dlp/v1/annotations/:annotationId` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/saas) |
| [Get Exfiltration Actor Activity](actions/get-exfiltration-actor-activity.md) | `GET /exfiltration/v1/actor/activity` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/exfiltration-prevention-apis) |
| [Get Exfiltration Asset Activity](actions/get-exfiltration-asset-activity.md) | `GET /exfiltration/v1/asset/activity` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/exfiltration-prevention-apis) |
| [Get Exfiltration Event](actions/get-exfiltration-event.md) | `GET /exfiltration/v1/events/:eventId` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/exfiltration-prevention-apis) |
| [Get Exfiltration Event Activity](actions/get-exfiltration-event-activity.md) | `GET /exfiltration/v1/events/:eventId/activity` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/exfiltration-prevention-apis) |
| [Get Posture Actor Activity](actions/get-posture-actor-activity.md) | `GET /posture/v1/actor/activity` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/posture-management-apis) |
| [Get Posture Asset Activity](actions/get-posture-asset-activity.md) | `GET /posture/v1/asset/activity` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/posture-management-apis) |
| [Get Posture Event](actions/get-posture-event.md) | `GET /posture/v1/events/:eventId` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/posture-management-apis) |
| [Get Posture Event Activity](actions/get-posture-event-activity.md) | `GET /posture/v1/events/:eventId/activity` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/posture-management-apis) |
| [Get Violation](actions/get-violation.md) | `GET /dlp/v1/violations/:violationId` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/saas) |
| [Get Violation Activity](actions/get-violation-activity.md) | `GET /dlp/v1/violations/:violationId/activity` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/saas) |
| [Get Violation Findings](actions/get-violation-findings.md) | `GET /dlp/v1/violations/:violationId/findings` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/saas) |
| [List Endpoint Devices](actions/list-endpoint-devices.md) | `GET /apps/v1/endpoint/devices` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/saas-app-and-device-management-apis) |
| [List Exfiltration Events](actions/list-exfiltration-events.md) | `GET /exfiltration/v1/events` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/exfiltration-prevention-apis) |
| [List GitHub Repositories](actions/list-git-hub-repositories.md) | `GET /apps/v1/github/repositories` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/saas-app-and-device-management-apis) |
| [List Posture Events](actions/list-posture-events.md) | `GET /posture/v1/events` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/posture-management-apis) |
| [List Violations](actions/list-violations.md) | `GET /dlp/v1/violations` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/saas) |
| [Remove Finding Annotation](actions/remove-finding-annotation.md) | `POST /dlp/v1/findings/:findingId/unannotate` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/saas) |
| [Scan Text](actions/scan-text.md) | `POST /v3/scan` | [docs](https://help.nightfall.ai/developer-api/introduction/quickstart) |
| [Scan Uploaded File](actions/scan-uploaded-file.md) | `POST /v3/upload/:fileId/scan` | [docs](https://help.nightfall.ai/developer-api/key-concepts/file_scan/scan_api_calls) |
| [Search Exfiltration Events](actions/search-exfiltration-events.md) | `GET /exfiltration/v1/events/search` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/exfiltration-prevention-apis) |
| [Search Posture Events](actions/search-posture-events.md) | `GET /posture/v1/events/search` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/posture-management-apis) |
| [Search Violations](actions/search-violations.md) | `GET /dlp/v1/violations/search` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/saas) |
| [Take Action on Violations](actions/take-action-on-violations.md) | `POST /dlp/v1/violations/actions` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/saas) |
| [Update Policy Domain Scope](actions/update-policy-domain-scope.md) | `POST /policy/v1/:policyID/scope/domains` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/scope_update) |
| [Update Policy User Scope](actions/update-policy-user-scope.md) | `POST /policy/v1/:policyID/scope/users` | [docs](https://help.nightfall.ai/developer-api/nightfall_apis/scope_update) |
| [Upload File Chunk](actions/upload-file-chunk.md) | `PATCH /v3/upload/:fileId` | [docs](https://help.nightfall.ai/developer-api/key-concepts/file_scan/scan_api_calls) |
