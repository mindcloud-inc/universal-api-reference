# jo4.io: Native API Reference

A consolidated summary of jo4.io's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://jo4-api.jo4.io/swagger-ui/index.html
- **OpenAPI specification:** https://jo4-api.jo4.io/v3/api-docs
- **API base URL:** `https://jo4-api.jo4.io/api/v1`

## Authentication

### API Key

Authenticate with the X-Jo4-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Jo4-API-Key: <apiKey>
```

[Official authentication documentation](https://jo4-api.jo4.io/swagger-ui/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `size` in the query string to set the page size (default 30). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Domain](actions/add-domain.md) | `POST /protected/domains` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/custom-domain-controller/addDomain) |
| [Add A/B Test Variant](actions/add-variant.md) | `POST /protected/url/:slug/ab-test/variants` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/ab-test-controller/addVariant) |
| [Approve Transfer Request](actions/approve-request.md) | `POST /protected/transfer-request/:slug/approve` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/url-transfer-request-controller/approveRequest) |
| [Bulk Import URLs](actions/bulk-import.md) | `POST /protected/url/bulk-import` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/url-controller/bulkImport) |
| [Create A/B Test](actions/create-ab-test.md) | `POST /protected/url/:slug/ab-test` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/ab-test-controller/createAbTest) |
| [Create API Key](actions/create-api-key.md) | `POST /protected/api-keys` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/api-key-controller/createApiKey) |
| [Create Transfer Request](actions/create-request.md) | `POST /protected/transfer-request` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/url-transfer-request-controller/createRequest) |
| [Create Team](actions/create-team.md) | `POST /protected/teams` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/team-controller/createTeam) |
| [Create URL](actions/create-url.md) | `POST /protected/url` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/url-controller/createUrl) |
| [Create Webhook](actions/create-webhook.md) | `POST /protected/webhooks` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/webhook-controller/createWebhook) |
| [Declare A/B Test Winner](actions/declare-winner.md) | `POST /protected/url/:slug/ab-test/winner/:variantId` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/ab-test-controller/declareWinner) |
| [Delete URL](actions/delete-url.md) | `DELETE /protected/url/:id` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/url-controller/deleteUrl) |
| [Get A/B Test Stats](actions/get-ab-test-stats.md) | `GET /protected/url/:slug/ab-test` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/ab-test-controller/getAbTestStats) |
| [List Conversions](actions/get-conversions.md) | `GET /protected/url/:slug/conversions` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/conversion-controller/getConversions) |
| [List Domains](actions/get-domains.md) | `GET /protected/domains` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/custom-domain-controller/getDomains) |
| [List Team Invitations](actions/get-invitations.md) | `GET /protected/teams/:teamSlug/invitations` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/team-controller/getInvitations) |
| [List My Teams](actions/get-my-teams.md) | `GET /protected/teams` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/team-controller/getMyTeams) |
| [List My URLs](actions/get-my-urls.md) | `GET /protected/url/myurls` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/url-controller/getMyUrls) |
| [List My Webhooks](actions/get-my-webhooks.md) | `GET /protected/webhooks` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/webhook-controller/getMyWebhooks) |
| [List A/B Test Variants](actions/get-variants.md) | `GET /protected/url/:slug/ab-test/variants` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/ab-test-controller/getVariants) |
| [Invite Member](actions/invite-member.md) | `POST /protected/teams/:teamSlug/invitations` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/team-controller/inviteMember) |
| [List API Keys](actions/list-api-keys.md) | `GET /protected/api-keys` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/api-key-controller/listApiKeys) |
| [Pause A/B Test](actions/pause-ab-test.md) | `POST /protected/url/:slug/ab-test/pause` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/ab-test-controller/pauseAbTest) |
| [Promote A/B Test Winner](actions/promote-winner.md) | `POST /protected/url/:slug/ab-test/promote` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/ab-test-controller/promoteWinner) |
| [Record Conversion](actions/record-conversion-1.md) | `POST /protected/url/:slug/conversions` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/conversion-controller/recordConversion_1) |
| [Refresh URL Metadata](actions/refresh-metadata.md) | `POST /protected/url/:id/refresh-metadata` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/url-controller/refreshMetadata) |
| [Reject Transfer Request](actions/reject-request.md) | `POST /protected/transfer-request/:slug/reject` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/url-transfer-request-controller/rejectRequest) |
| [Resume A/B Test](actions/resume-ab-test.md) | `POST /protected/url/:slug/ab-test/resume` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/ab-test-controller/resumeAbTest) |
| [Update URL](actions/update-url.md) | `PUT /protected/url/:id` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/url-controller/updateUrl) |
| [Verify Domain](actions/verify-domain.md) | `POST /protected/domains/:id/verify` | [docs](https://jo4-api.jo4.io/swagger-ui/index.html#/custom-domain-controller/verifyDomain) |
