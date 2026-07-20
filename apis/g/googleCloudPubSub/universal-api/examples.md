# Google Cloud Pub/Sub Universal API Examples

These examples use the MindCloud API key and Google Cloud Pub/Sub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Topics

Retrieves topics from Google Cloud Pub/Sub.

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

Example response:

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

See the full [List Topics action reference](actions/list-topics.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleCloudPubSub/latest/actions/list-topics).

## Acknowledge Messages

Acknowledges subscription messages in Google Cloud Pub/Sub.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/acknowledge-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscription": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/acknowledge-messages', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscription": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Acknowledge Messages action reference](actions/acknowledge-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleCloudPubSub/latest/actions/acknowledge-messages).
