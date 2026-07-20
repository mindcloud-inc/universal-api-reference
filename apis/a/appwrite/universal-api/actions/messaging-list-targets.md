# Appwrite: List message targets

Retrieves a list of message targets from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-list-targets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-list-targets?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-list-targets?${params}`, {
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
| `messageId` | string | yes | Message ID. |
| `queries[]` | array<string> | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. You may filter on the following attributes: userId, providerId, identifier, providerType Accepts multiple values as an array. |
| `total` | boolean | no | When set to false, the total count returned will be 0 and will not be calculated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "targets": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `targets` | array<object> | List of targets. |
| `total` | number | Total number of targets that matched your query. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /messaging/messages/{messageId}/targets` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/messaging-list-targets.md) for the provider-specific parameters and requirements.

