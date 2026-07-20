# Google Cloud Pub/Sub: Set Schema IAM Policy

Sets a schema IAM policy in Google Cloud Pub/Sub.

```
PUT https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/set-schema-iam-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/set-schema-iam-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resource": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/set-schema-iam-policy', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resource": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resource` | string | yes | REQUIRED: The resource for which the policy is being specified. See [Resource names](https://cloud.google.com/apis/design/resource_names) for the appropriate value for this field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bindings": [
        {
          "condition": {
            "description": "string",
            "expression": "string",
            "location": "string",
            "title": "string"
          },
          "members": [
            [
              "string"
            ]
          ],
          "role": "string"
        }
      ],
      "etag": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bindings[].condition.description` | string |  |
| `bindings[].condition.expression` | string |  |
| `bindings[].condition.location` | string |  |
| `bindings[].condition.title` | string |  |
| `bindings[].members[]` | array<string> |  |
| `bindings[].role` | string |  |
| `etag` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `POST /v1/:resource:setIamPolicy` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-schema-iam-policy.md) for the provider-specific parameters and requirements.

