# Google Cloud Pub/Sub: List Topics

Retrieves topics from Google Cloud Pub/Sub.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-topics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-topics?connectionId=$CONNECTION_ID&limit=25&offset=0&project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-topics?${params}`, {
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
| `project` | string | yes | Required. The name of the project in which to list topics. Format is `projects/{project-id}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "topics": [
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
| `topics[].ingestionDataSourceSettings.awsKinesis.awsRoleArn` | string |  |
| `topics[].ingestionDataSourceSettings.awsKinesis.consumerArn` | string |  |
| `topics[].ingestionDataSourceSettings.awsKinesis.gcpServiceAccount` | string |  |
| `topics[].ingestionDataSourceSettings.awsKinesis.state` | string |  |
| `topics[].ingestionDataSourceSettings.awsKinesis.streamArn` | string |  |
| `topics[].ingestionDataSourceSettings.awsMsk.awsRoleArn` | string |  |
| `topics[].ingestionDataSourceSettings.awsMsk.clusterArn` | string |  |
| `topics[].ingestionDataSourceSettings.awsMsk.gcpServiceAccount` | string |  |
| `topics[].ingestionDataSourceSettings.awsMsk.state` | string |  |
| `topics[].ingestionDataSourceSettings.awsMsk.topic` | string |  |
| `topics[].ingestionDataSourceSettings.azureEventHubs.clientId` | string |  |
| `topics[].ingestionDataSourceSettings.azureEventHubs.eventHub` | string |  |
| `topics[].ingestionDataSourceSettings.azureEventHubs.gcpServiceAccount` | string |  |
| `topics[].ingestionDataSourceSettings.azureEventHubs.namespace` | string |  |
| `topics[].ingestionDataSourceSettings.azureEventHubs.resourceGroup` | string |  |
| `topics[].ingestionDataSourceSettings.azureEventHubs.state` | string |  |
| `topics[].ingestionDataSourceSettings.azureEventHubs.subscriptionId` | string |  |
| `topics[].ingestionDataSourceSettings.azureEventHubs.tenantId` | string |  |
| `topics[].ingestionDataSourceSettings.cloudStorage.bucket` | string |  |
| `topics[].ingestionDataSourceSettings.cloudStorage.matchGlob` | string |  |
| `topics[].ingestionDataSourceSettings.cloudStorage.minimumObjectCreateTime` | string |  |
| `topics[].ingestionDataSourceSettings.cloudStorage.state` | string |  |
| `topics[].ingestionDataSourceSettings.cloudStorage.textFormat.delimiter` | string |  |
| `topics[].ingestionDataSourceSettings.confluentCloud.bootstrapServer` | string |  |
| `topics[].ingestionDataSourceSettings.confluentCloud.clusterId` | string |  |
| `topics[].ingestionDataSourceSettings.confluentCloud.gcpServiceAccount` | string |  |
| `topics[].ingestionDataSourceSettings.confluentCloud.identityPoolId` | string |  |
| `topics[].ingestionDataSourceSettings.confluentCloud.state` | string |  |
| `topics[].ingestionDataSourceSettings.confluentCloud.topic` | string |  |
| `topics[].ingestionDataSourceSettings.platformLogsSettings.severity` | string |  |
| `topics[].kmsKeyName` | string |  |
| `topics[].messageRetentionDuration` | string |  |
| `topics[].messageStoragePolicy.allowedPersistenceRegions[]` | array<string> |  |
| `topics[].messageStoragePolicy.enforceInTransit` | boolean |  |
| `topics[].messageTransforms[].aiInference.endpoint` | string |  |
| `topics[].messageTransforms[].aiInference.serviceAccountEmail` | string |  |
| `topics[].messageTransforms[].disabled` | boolean |  |
| `topics[].messageTransforms[].enabled` | boolean |  |
| `topics[].messageTransforms[].javascriptUdf.code` | string |  |
| `topics[].messageTransforms[].javascriptUdf.functionName` | string |  |
| `topics[].name` | string |  |
| `topics[].satisfiesPzs` | boolean |  |
| `topics[].schemaSettings.encoding` | string |  |
| `topics[].schemaSettings.firstRevisionId` | string |  |
| `topics[].schemaSettings.lastRevisionId` | string |  |
| `topics[].schemaSettings.schema` | string |  |
| `topics[].state` | string |  |

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `GET /v1/:project/topics` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-topics.md) for the provider-specific parameters and requirements.

