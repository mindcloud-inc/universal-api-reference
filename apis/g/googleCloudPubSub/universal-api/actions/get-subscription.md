# Google Cloud Pub/Sub: Get Subscription

Retrieves a subscription from Google Cloud Pub/Sub.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-subscription?connectionId=$CONNECTION_ID&subscription=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscription": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-subscription?${params}`, {
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
| `subscription` | string | yes | Required. The name of the subscription to get. Format is `projects/{project}/subscriptions/{sub}`. |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ackDeadlineSeconds` | number |  |
| `analyticsHubSubscriptionInfo.listing` | string |  |
| `analyticsHubSubscriptionInfo.subscription` | string |  |
| `bigqueryConfig.dropUnknownFields` | boolean |  |
| `bigqueryConfig.serviceAccountEmail` | string |  |
| `bigqueryConfig.state` | string |  |
| `bigqueryConfig.table` | string |  |
| `bigqueryConfig.useTableSchema` | boolean |  |
| `bigqueryConfig.useTopicSchema` | boolean |  |
| `bigqueryConfig.writeMetadata` | boolean |  |
| `bigtableConfig.appProfileId` | string |  |
| `bigtableConfig.serviceAccountEmail` | string |  |
| `bigtableConfig.state` | string |  |
| `bigtableConfig.table` | string |  |
| `bigtableConfig.writeMetadata` | boolean |  |
| `cloudStorageConfig.avroConfig.useTopicSchema` | boolean |  |
| `cloudStorageConfig.avroConfig.writeMetadata` | boolean |  |
| `cloudStorageConfig.bucket` | string |  |
| `cloudStorageConfig.filenameDatetimeFormat` | string |  |
| `cloudStorageConfig.filenamePrefix` | string |  |
| `cloudStorageConfig.filenameSuffix` | string |  |
| `cloudStorageConfig.maxBytes` | string |  |
| `cloudStorageConfig.maxDuration` | string |  |
| `cloudStorageConfig.maxMessages` | string |  |
| `cloudStorageConfig.serviceAccountEmail` | string |  |
| `cloudStorageConfig.state` | string |  |
| `deadLetterPolicy.deadLetterTopic` | string |  |
| `deadLetterPolicy.maxDeliveryAttempts` | number |  |
| `detached` | boolean |  |
| `enableExactlyOnceDelivery` | boolean |  |
| `enableMessageOrdering` | boolean |  |
| `expirationPolicy.ttl` | string |  |
| `filter` | string |  |
| `messageRetentionDuration` | string |  |
| `messageTransforms[].aiInference.endpoint` | string |  |
| `messageTransforms[].aiInference.serviceAccountEmail` | string |  |
| `messageTransforms[].disabled` | boolean |  |
| `messageTransforms[].enabled` | boolean |  |
| `messageTransforms[].javascriptUdf.code` | string |  |
| `messageTransforms[].javascriptUdf.functionName` | string |  |
| `name` | string |  |
| `pushConfig.noWrapper.writeMetadata` | boolean |  |
| `pushConfig.oidcToken.audience` | string |  |
| `pushConfig.oidcToken.serviceAccountEmail` | string |  |
| `pushConfig.pushEndpoint` | string |  |
| `retainAckedMessages` | boolean |  |
| `retryPolicy.maximumBackoff` | string |  |
| `retryPolicy.minimumBackoff` | string |  |
| `state` | string |  |
| `topic` | string |  |
| `topicMessageRetentionDuration` | string |  |

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `GET /v1/:subscription` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription.md) for the provider-specific parameters and requirements.

