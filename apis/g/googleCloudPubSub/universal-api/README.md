# <img src="https://images.mindcloud.co/apps/icons/google-cloud-pub-sub_1776962753808.png" alt="Google Cloud Pub/Sub logo" width="28" height="28"> Google Cloud Pub/Sub: Universal API

Publish, subscribe, and manage Pub/Sub topics, subscriptions, and schemas

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleCloudPubSub/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 46
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloud.google.com/pubsub
- **Vendor API docs:** https://docs.cloud.google.com/pubsub/docs/reference/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Topics](actions/list-topics.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-topics?connectionId=$CONNECTION_ID&limit=25&offset=0&project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (46)

### Schema

| Action | Method | Description |
| --- | --- | --- |
| [Commit Schema Revision](actions/commit-schema-revision.md) | PUT | Commits a new schema revision in Google Cloud Pub/Sub. |
| [Create Schema](actions/create-schema.md) | POST | Creates a schema in Google Cloud Pub/Sub. |
| [Delete Schema](actions/delete-schema.md) | DELETE | Deletes a schema from Google Cloud Pub/Sub. |
| [Delete Schema Revision](actions/delete-schema-revision.md) | DELETE | Deletes a schema revision from Google Cloud Pub/Sub. |
| [Get Schema](actions/get-schema.md) | GET | Retrieves a schema from Google Cloud Pub/Sub. |
| [Get Schema IAM Policy](actions/get-schema-iam-policy.md) | GET | Retrieves a schema IAM policy from Google Cloud Pub/Sub. |
| [List Schema Revisions](actions/list-schema-revisions.md) | GET | Retrieves schema revisions from Google Cloud Pub/Sub. |
| [List Schemas](actions/list-schemas.md) | GET | Retrieves schemas from Google Cloud Pub/Sub. |
| [Roll Back Schema Revision](actions/roll-back-schema-revision.md) | PUT | Rolls back a schema revision in Google Cloud Pub/Sub. |
| [Set Schema IAM Policy](actions/set-schema-iam-policy.md) | PUT | Sets a schema IAM policy in Google Cloud Pub/Sub. |
| [Test Schema IAM Permissions](actions/test-schema-iam-permissions.md) | GET | Tests schema IAM permissions in Google Cloud Pub/Sub. |
| [Validate Message Against Schema](actions/validate-message-against-schema.md) | GET | Validates a message against a schema in Google Cloud Pub/Sub. |
| [Validate Schema](actions/validate-schema.md) | GET | Validates a schema in Google Cloud Pub/Sub. |

### Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Create Snapshot](actions/create-snapshot.md) | POST | Creates a snapshot in Google Cloud Pub/Sub. |
| [Delete Snapshot](actions/delete-snapshot.md) | DELETE | Deletes a snapshot from Google Cloud Pub/Sub. |
| [Get Snapshot](actions/get-snapshot.md) | GET | Retrieves a snapshot from Google Cloud Pub/Sub. |
| [Get Snapshot IAM Policy](actions/get-snapshot-iam-policy.md) | GET | Retrieves a snapshot IAM policy from Google Cloud Pub/Sub. |
| [List Snapshots](actions/list-snapshots.md) | GET | Retrieves snapshots from Google Cloud Pub/Sub. |
| [List Topic Snapshots](actions/list-topic-snapshots.md) | GET | Retrieves snapshots for a topic in Google Cloud Pub/Sub. |
| [Set Snapshot IAM Policy](actions/set-snapshot-iam-policy.md) | PUT | Sets a snapshot IAM policy in Google Cloud Pub/Sub. |
| [Test Snapshot IAM Permissions](actions/test-snapshot-iam-permissions.md) | GET | Tests snapshot IAM permissions in Google Cloud Pub/Sub. |
| [Update Snapshot](actions/update-snapshot.md) | PUT | Updates a snapshot in Google Cloud Pub/Sub. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Acknowledge Messages](actions/acknowledge-messages.md) | PUT | Acknowledges subscription messages in Google Cloud Pub/Sub. |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a subscription in Google Cloud Pub/Sub. |
| [Delete Subscription](actions/delete-subscription.md) | DELETE | Deletes a subscription from Google Cloud Pub/Sub. |
| [Detach Subscription](actions/detach-subscription.md) | PUT | Detaches a subscription from its topic in Google Cloud Pub/Sub. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from Google Cloud Pub/Sub. |
| [Get Subscription IAM Policy](actions/get-subscription-iam-policy.md) | GET | Retrieves a subscription IAM policy from Google Cloud Pub/Sub. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Google Cloud Pub/Sub. |
| [List Topic Subscriptions](actions/list-topic-subscriptions.md) | GET | Retrieves subscriptions for a topic in Google Cloud Pub/Sub. |
| [Modify Ack Deadline](actions/modify-ack-deadline.md) | PUT | Modifies a subscription ack deadline in Google Cloud Pub/Sub. |
| [Modify Push Config](actions/modify-push-config.md) | PUT | Modifies a subscription push config in Google Cloud Pub/Sub. |
| [Pull Messages](actions/pull-messages.md) | GET | Pulls messages from Google Cloud Pub/Sub. |
| [Seek Subscription](actions/seek-subscription.md) | PUT | Seeks a subscription to a timestamp or snapshot in Google Cloud Pub/Sub. |
| [Set Subscription IAM Policy](actions/set-subscription-iam-policy.md) | PUT | Sets a subscription IAM policy in Google Cloud Pub/Sub. |
| [Test Subscription IAM Permissions](actions/test-subscription-iam-permissions.md) | GET | Tests subscription IAM permissions in Google Cloud Pub/Sub. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates a subscription in Google Cloud Pub/Sub. |

### Topic

| Action | Method | Description |
| --- | --- | --- |
| [Create Topic](actions/create-topic.md) | POST | Creates a topic in Google Cloud Pub/Sub. |
| [Delete Topic](actions/delete-topic.md) | DELETE | Deletes a topic from Google Cloud Pub/Sub. |
| [Get Topic](actions/get-topic.md) | GET | Retrieves a topic from Google Cloud Pub/Sub. |
| [Get Topic IAM Policy](actions/get-topic-iam-policy.md) | GET | Retrieves a topic IAM policy from Google Cloud Pub/Sub. |
| [List Topics](actions/list-topics.md) | GET | Retrieves topics from Google Cloud Pub/Sub. |
| [Publish Messages](actions/publish-messages.md) | POST | Publishes messages to a topic in Google Cloud Pub/Sub. |
| [Set Topic IAM Policy](actions/set-topic-iam-policy.md) | PUT | Sets a topic IAM policy in Google Cloud Pub/Sub. |
| [Test Topic IAM Permissions](actions/test-topic-iam-permissions.md) | GET | Tests topic IAM permissions in Google Cloud Pub/Sub. |
| [Update Topic](actions/update-topic.md) | PUT | Updates a topic in Google Cloud Pub/Sub. |

