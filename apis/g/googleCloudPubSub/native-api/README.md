# Google Cloud Pub/Sub: Native API Reference

A consolidated summary of Google Cloud Pub/Sub's API configuration and 46 documented operations, with links to official documentation.

- **Official docs:** https://docs.cloud.google.com/pubsub/docs/reference/rest
- **API base URL:** `https://pubsub.googleapis.com`

## Authentication

### OAuth 2.0

Authorize Google Cloud Pub/Sub with a Google OAuth 2.0 web application.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/pubsub https://www.googleapis.com/auth/cloud-platform`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/web-server)

### Service Account

Authenticate Google Cloud Pub/Sub with a Google Cloud service account private key.

### Credentials

- **Project ID:** `project` · required · The Google Cloud project ID that contains the Pub/Sub resources this connection should access.
- **Client Email:** `clientEmail` · required · The client_email value from the service account key JSON file.
- **Private Key ID:** `privateKeyId` · optional · Optional legacy field from the service account key JSON file. The Google auth SDK can mint Pub/Sub access tokens with only project ID, client email, and private key.
- **Private Key:** `privateKeySecret` · required · The private_key value from the service account key JSON file. MindCloud uses it only to sign short-lived Google OAuth JWT assertions.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/service-account)

## Pagination

Use `pageSize` in the query string to set the page size. Use `pageToken` in the query string as the pagination cursor.

## Endpoints (46 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Acknowledge Messages](actions/acknowledge-messages.md) | `POST /v1/:subscription:acknowledge` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/acknowledge) |
| [Commit Schema Revision](actions/commit-schema-revision.md) | `POST /v1/:name:commit` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/commit) |
| [Create Schema](actions/create-schema.md) | `POST /v1/:parent/schemas` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/create) |
| [Create Snapshot](actions/create-snapshot.md) | `PUT /v1/:name` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.snapshots/create) |
| [Create Subscription](actions/create-subscription.md) | `PUT /v1/:name` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/create) |
| [Create Topic](actions/create-topic.md) | `PUT /v1/:name` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/create) |
| [Delete Schema](actions/delete-schema.md) | `DELETE /v1/:name` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/delete) |
| [Delete Schema Revision](actions/delete-schema-revision.md) | `DELETE /v1/:name:deleteRevision` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/deleteRevision) |
| [Delete Snapshot](actions/delete-snapshot.md) | `DELETE /v1/:snapshot` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.snapshots/delete) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE /v1/:subscription` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/delete) |
| [Delete Topic](actions/delete-topic.md) | `DELETE /v1/:topic` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/delete) |
| [Detach Subscription](actions/detach-subscription.md) | `POST /v1/:subscription:detach` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/detach) |
| [Get Schema](actions/get-schema.md) | `GET /v1/:name` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/get) |
| [Get Schema IAM Policy](actions/get-schema-iam-policy.md) | `GET /v1/:resource:getIamPolicy` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/getIamPolicy) |
| [Get Snapshot](actions/get-snapshot.md) | `GET /v1/:snapshot` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.snapshots/get) |
| [Get Snapshot IAM Policy](actions/get-snapshot-iam-policy.md) | `GET /v1/:resource:getIamPolicy` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.snapshots/getIamPolicy) |
| [Get Subscription](actions/get-subscription.md) | `GET /v1/:subscription` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/get) |
| [Get Subscription IAM Policy](actions/get-subscription-iam-policy.md) | `GET /v1/:resource:getIamPolicy` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/getIamPolicy) |
| [Get Topic](actions/get-topic.md) | `GET /v1/:topic` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/get) |
| [Get Topic IAM Policy](actions/get-topic-iam-policy.md) | `GET /v1/:resource:getIamPolicy` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/getIamPolicy) |
| [List Schema Revisions](actions/list-schema-revisions.md) | `GET /v1/:name:listRevisions` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/listRevisions) |
| [List Schemas](actions/list-schemas.md) | `GET /v1/:parent/schemas` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/list) |
| [List Snapshots](actions/list-snapshots.md) | `GET /v1/:project/snapshots` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.snapshots/list) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /v1/:project/subscriptions` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/list) |
| [List Topic Snapshots](actions/list-topic-snapshots.md) | `GET /v1/:topic/snapshots` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics.snapshots/list) |
| [List Topic Subscriptions](actions/list-topic-subscriptions.md) | `GET /v1/:topic/subscriptions` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics.subscriptions/list) |
| [List Topics](actions/list-topics.md) | `GET /v1/:project/topics` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/list) |
| [Modify Ack Deadline](actions/modify-ack-deadline.md) | `POST /v1/:subscription:modifyAckDeadline` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/modifyAckDeadline) |
| [Modify Push Config](actions/modify-push-config.md) | `POST /v1/:subscription:modifyPushConfig` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/modifyPushConfig) |
| [Publish Messages](actions/publish-messages.md) | `POST /v1/:topic:publish` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/publish) |
| [Pull Messages](actions/pull-messages.md) | `POST /v1/:subscription:pull` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/pull) |
| [Roll Back Schema Revision](actions/roll-back-schema-revision.md) | `POST /v1/:name:rollback` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/rollback) |
| [Seek Subscription](actions/seek-subscription.md) | `POST /v1/:subscription:seek` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/seek) |
| [Set Schema IAM Policy](actions/set-schema-iam-policy.md) | `POST /v1/:resource:setIamPolicy` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/setIamPolicy) |
| [Set Snapshot IAM Policy](actions/set-snapshot-iam-policy.md) | `POST /v1/:resource:setIamPolicy` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.snapshots/setIamPolicy) |
| [Set Subscription IAM Policy](actions/set-subscription-iam-policy.md) | `POST /v1/:resource:setIamPolicy` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/setIamPolicy) |
| [Set Topic IAM Policy](actions/set-topic-iam-policy.md) | `POST /v1/:resource:setIamPolicy` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/setIamPolicy) |
| [Test Schema IAM Permissions](actions/test-schema-iam-permissions.md) | `POST /v1/:resource:testIamPermissions` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/testIamPermissions) |
| [Test Snapshot IAM Permissions](actions/test-snapshot-iam-permissions.md) | `POST /v1/:resource:testIamPermissions` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.snapshots/testIamPermissions) |
| [Test Subscription IAM Permissions](actions/test-subscription-iam-permissions.md) | `POST /v1/:resource:testIamPermissions` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/testIamPermissions) |
| [Test Topic IAM Permissions](actions/test-topic-iam-permissions.md) | `POST /v1/:resource:testIamPermissions` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/testIamPermissions) |
| [Update Snapshot](actions/update-snapshot.md) | `PATCH /v1/:name` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.snapshots/patch) |
| [Update Subscription](actions/update-subscription.md) | `PATCH /v1/:name` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.subscriptions/patch) |
| [Update Topic](actions/update-topic.md) | `PATCH /v1/:name` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.topics/patch) |
| [Validate Message Against Schema](actions/validate-message-against-schema.md) | `POST /v1/:parent/schemas:validateMessage` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/validateMessage) |
| [Validate Schema](actions/validate-schema.md) | `POST /v1/:parent/schemas:validate` | [docs](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/validate) |
