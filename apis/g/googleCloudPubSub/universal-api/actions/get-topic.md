# Google Cloud Pub/Sub: Get Topic

Retrieves a topic from Google Cloud Pub/Sub.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-topic?connectionId=$CONNECTION_ID&topic=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topic": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-topic?${params}`, {
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
| `topic` | string | yes | Required. The name of the topic to get. Format is `projects/{project}/topics/{topic}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ingestionDataSourceSettings": {
        "awsKinesis": {
          "awsRoleArn": "string",
          "consumerArn": "string",
          "gcpServiceAccount": "string",
          "state": "string",
          "streamArn": "string"
        },
        "awsMsk": {
          "awsRoleArn": "string",
          "clusterArn": "string",
          "gcpServiceAccount": "string",
          "state": "string",
          "topic": "string"
        },
        "azureEventHubs": {
          "clientId": "string",
          "eventHub": "string",
          "gcpServiceAccount": "string",
          "namespace": "Ava Chen",
          "resourceGroup": "string",
          "state": "string",
          "subscriptionId": "string",
          "tenantId": "string"
        },
        "cloudStorage": {
          "bucket": "string",
          "matchGlob": "string",
          "minimumObjectCreateTime": "string",
          "state": "string",
          "textFormat": {
            "delimiter": "string"
          }
        },
        "confluentCloud": {
          "bootstrapServer": "string",
          "clusterId": "string",
          "gcpServiceAccount": "string",
          "identityPoolId": "string",
          "state": "string",
          "topic": "string"
        },
        "platformLogsSettings": {
          "severity": "string"
        }
      },
      "kmsKeyName": "Ava Chen",
      "messageRetentionDuration": "string",
      "messageStoragePolicy": {
        "allowedPersistenceRegions": [
          [
            "string"
          ]
        ],
        "enforceInTransit": true
      },
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
      "satisfiesPzs": true,
      "schemaSettings": {
        "encoding": "string",
        "firstRevisionId": "string",
        "lastRevisionId": "string",
        "schema": "string"
      },
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ingestionDataSourceSettings.awsKinesis.awsRoleArn` | string |  |
| `ingestionDataSourceSettings.awsKinesis.consumerArn` | string |  |
| `ingestionDataSourceSettings.awsKinesis.gcpServiceAccount` | string |  |
| `ingestionDataSourceSettings.awsKinesis.state` | string |  |
| `ingestionDataSourceSettings.awsKinesis.streamArn` | string |  |
| `ingestionDataSourceSettings.awsMsk.awsRoleArn` | string |  |
| `ingestionDataSourceSettings.awsMsk.clusterArn` | string |  |
| `ingestionDataSourceSettings.awsMsk.gcpServiceAccount` | string |  |
| `ingestionDataSourceSettings.awsMsk.state` | string |  |
| `ingestionDataSourceSettings.awsMsk.topic` | string |  |
| `ingestionDataSourceSettings.azureEventHubs.clientId` | string |  |
| `ingestionDataSourceSettings.azureEventHubs.eventHub` | string |  |
| `ingestionDataSourceSettings.azureEventHubs.gcpServiceAccount` | string |  |
| `ingestionDataSourceSettings.azureEventHubs.namespace` | string |  |
| `ingestionDataSourceSettings.azureEventHubs.resourceGroup` | string |  |
| `ingestionDataSourceSettings.azureEventHubs.state` | string |  |
| `ingestionDataSourceSettings.azureEventHubs.subscriptionId` | string |  |
| `ingestionDataSourceSettings.azureEventHubs.tenantId` | string |  |
| `ingestionDataSourceSettings.cloudStorage.bucket` | string |  |
| `ingestionDataSourceSettings.cloudStorage.matchGlob` | string |  |
| `ingestionDataSourceSettings.cloudStorage.minimumObjectCreateTime` | string |  |
| `ingestionDataSourceSettings.cloudStorage.state` | string |  |
| `ingestionDataSourceSettings.cloudStorage.textFormat.delimiter` | string |  |
| `ingestionDataSourceSettings.confluentCloud.bootstrapServer` | string |  |
| `ingestionDataSourceSettings.confluentCloud.clusterId` | string |  |
| `ingestionDataSourceSettings.confluentCloud.gcpServiceAccount` | string |  |
| `ingestionDataSourceSettings.confluentCloud.identityPoolId` | string |  |
| `ingestionDataSourceSettings.confluentCloud.state` | string |  |
| `ingestionDataSourceSettings.confluentCloud.topic` | string |  |
| `ingestionDataSourceSettings.platformLogsSettings.severity` | string |  |
| `kmsKeyName` | string |  |
| `messageRetentionDuration` | string |  |
| `messageStoragePolicy.allowedPersistenceRegions[]` | array<string> |  |
| `messageStoragePolicy.enforceInTransit` | boolean |  |
| `messageTransforms[].aiInference.endpoint` | string |  |
| `messageTransforms[].aiInference.serviceAccountEmail` | string |  |
| `messageTransforms[].disabled` | boolean |  |
| `messageTransforms[].enabled` | boolean |  |
| `messageTransforms[].javascriptUdf.code` | string |  |
| `messageTransforms[].javascriptUdf.functionName` | string |  |
| `name` | string |  |
| `satisfiesPzs` | boolean |  |
| `schemaSettings.encoding` | string |  |
| `schemaSettings.firstRevisionId` | string |  |
| `schemaSettings.lastRevisionId` | string |  |
| `schemaSettings.schema` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `GET /v1/:topic` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-topic.md) for the provider-specific parameters and requirements.

