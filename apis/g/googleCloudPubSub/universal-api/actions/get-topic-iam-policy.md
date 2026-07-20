# Google Cloud Pub/Sub: Get Topic IAM Policy

Retrieves a topic IAM policy from Google Cloud Pub/Sub.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-topic-iam-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-topic-iam-policy?connectionId=$CONNECTION_ID&resource=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resource": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-topic-iam-policy?${params}`, {
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
| `resource` | string | yes | REQUIRED: The resource for which the policy is being requested. See [Resource names](https://cloud.google.com/apis/design/resource_names) for the appropriate value for this field. |
| `optionsRequestedPolicyVersion` | number | no | Optional. The maximum policy version that will be used to format the policy. Valid values are 0, 1, and 3. |

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

Through the native Google Cloud Pub/Sub API, this operation is `GET /v1/:resource:getIamPolicy` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-topic-iam-policy.md) for the provider-specific parameters and requirements.

