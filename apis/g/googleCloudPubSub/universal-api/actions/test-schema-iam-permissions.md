# Google Cloud Pub/Sub: Test Schema IAM Permissions

Tests schema IAM permissions in Google Cloud Pub/Sub.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/test-schema-iam-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/test-schema-iam-permissions?connectionId=$CONNECTION_ID&resource=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resource": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/test-schema-iam-permissions?${params}`, {
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
| `resource` | string | yes | REQUIRED: The resource for which the policy detail is being requested. See [Resource names](https://cloud.google.com/apis/design/resource_names) for the appropriate value for this field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "permissions": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `permissions[]` | array<string> |  |

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `POST /v1/:resource:testIamPermissions` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-schema-iam-permissions.md) for the provider-specific parameters and requirements.

