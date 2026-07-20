# Google Cloud Pub/Sub: List Subscriptions

Retrieves subscriptions from Google Cloud Pub/Sub.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0&project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-subscriptions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | yes | Required. The name of the project in which to list subscriptions. Format is `projects/{project-id}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "subscriptions": [
        {
          "ackDeadlineSeconds": 1,
          "analyticsHubSubscriptionInfo": {
            "listing": "string",
            "subscription": "string"
          },
          "bigqueryConfig": {
            "dropUnknownFields": true,
            "serviceAccountEmail": "ava@example.com",
            "state": "string",
            "table": "string",
            "useTableSchema": true,
            "useTopicSchema": true,
            "writeMetadata": true
          },
          "bigtableConfig": {
            "appProfileId": "string",
            "serviceAccountEmail": "ava@example.com",
            "state": "string",
            "table": "string",
            "writeMetadata": true
          },
          "cloudStorageConfig": {
            "avroConfig": {
              "useTopicSchema": true,
              "writeMetadata": true
            },
            "bucket": "string",
            "filenameDatetimeFormat": "Ava Chen",
            "filenamePrefix": "Ava Chen",
            "filenameSuffix": "Ava Chen",
            "maxBytes": "string",
            "maxDuration": "string",
            "maxMessages": "string",
            "serviceAccountEmail": "ava@example.com",
            "state": "string"
          },
          "deadLetterPolicy": {
            "deadLetterTopic": "string",
            "maxDeliveryAttempts": 1
          },
          "detached": true,
          "enableExactlyOnceDelivery": true,
          "enableMessageOrdering": true,
          "expirationPolicy": {
            "ttl": "string"
          },
          "filter": "string",
          "messageRetentionDuration": "string",
          "messageTransforms": [
            {
              "aiInference": {
                "endpoint": "string",
                "serviceAccountEmail": "ava@example.com"
              },
              "disabled": true,
              "enabled": true,
              "javascriptUdf": {
                "code": "string",
                "functionName": "Ava Chen"
              }
            }
          ],
          "name": "Ava Chen",
          "pushConfig": {
            "noWrapper": {
              "writeMetadata": true
            },
            "oidcToken": {
              "audience": "string",
              "serviceAccountEmail": "ava@example.com"
            },
            "pushEndpoint": "string"
          },
          "retainAckedMessages": true,
          "retryPolicy": {
            "maximumBackoff": "string",
            "minimumBackoff": "string"
          },
          "state": "string",
          "topic": "string",
          "topicMessageRetentionDuration": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageToken` | string |  |
| `subscriptions[].ackDeadlineSeconds` | number |  |
| `subscriptions[].analyticsHubSubscriptionInfo.listing` | string |  |
| `subscriptions[].analyticsHubSubscriptionInfo.subscription` | string |  |
| `subscriptions[].bigqueryConfig.dropUnknownFields` | boolean |  |
| `subscriptions[].bigqueryConfig.serviceAccountEmail` | string |  |
| `subscriptions[].bigqueryConfig.state` | string |  |
| `subscriptions[].bigqueryConfig.table` | string |  |
| `subscriptions[].bigqueryConfig.useTableSchema` | boolean |  |
| `subscriptions[].bigqueryConfig.useTopicSchema` | boolean |  |
| `subscriptions[].bigqueryConfig.writeMetadata` | boolean |  |
| `subscriptions[].bigtableConfig.appProfileId` | string |  |
| `subscriptions[].bigtableConfig.serviceAccountEmail` | string |  |
| `subscriptions[].bigtableConfig.state` | string |  |
| `subscriptions[].bigtableConfig.table` | string |  |
| `subscriptions[].bigtableConfig.writeMetadata` | boolean |  |
| `subscriptions[].cloudStorageConfig.avroConfig.useTopicSchema` | boolean |  |
| `subscriptions[].cloudStorageConfig.avroConfig.writeMetadata` | boolean |  |
| `subscriptions[].cloudStorageConfig.bucket` | string |  |
| `subscriptions[].cloudStorageConfig.filenameDatetimeFormat` | string |  |
| `subscriptions[].cloudStorageConfig.filenamePrefix` | string |  |
| `subscriptions[].cloudStorageConfig.filenameSuffix` | string |  |
| `subscriptions[].cloudStorageConfig.maxBytes` | string |  |
| `subscriptions[].cloudStorageConfig.maxDuration` | string |  |
| `subscriptions[].cloudStorageConfig.maxMessages` | string |  |
| `subscriptions[].cloudStorageConfig.serviceAccountEmail` | string |  |
| `subscriptions[].cloudStorageConfig.state` | string |  |
| `subscriptions[].deadLetterPolicy.deadLetterTopic` | string |  |
| `subscriptions[].deadLetterPolicy.maxDeliveryAttempts` | number |  |
| `subscriptions[].detached` | boolean |  |
| `subscriptions[].enableExactlyOnceDelivery` | boolean |  |
| `subscriptions[].enableMessageOrdering` | boolean |  |
| `subscriptions[].expirationPolicy.ttl` | string |  |
| `subscriptions[].filter` | string |  |
| `subscriptions[].messageRetentionDuration` | string |  |
| `subscriptions[].messageTransforms[].aiInference.endpoint` | string |  |
| `subscriptions[].messageTransforms[].aiInference.serviceAccountEmail` | string |  |
| `subscriptions[].messageTransforms[].disabled` | boolean |  |
| `subscriptions[].messageTransforms[].enabled` | boolean |  |
| `subscriptions[].messageTransforms[].javascriptUdf.code` | string |  |
| `subscriptions[].messageTransforms[].javascriptUdf.functionName` | string |  |
| `subscriptions[].name` | string |  |
| `subscriptions[].pushConfig.noWrapper.writeMetadata` | boolean |  |
| `subscriptions[].pushConfig.oidcToken.audience` | string |  |
| `subscriptions[].pushConfig.oidcToken.serviceAccountEmail` | string |  |
| `subscriptions[].pushConfig.pushEndpoint` | string |  |
| `subscriptions[].retainAckedMessages` | boolean |  |
| `subscriptions[].retryPolicy.maximumBackoff` | string |  |
| `subscriptions[].retryPolicy.minimumBackoff` | string |  |
| `subscriptions[].state` | string |  |
| `subscriptions[].topic` | string |  |
| `subscriptions[].topicMessageRetentionDuration` | string |  |

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `GET /v1/:project/subscriptions` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

