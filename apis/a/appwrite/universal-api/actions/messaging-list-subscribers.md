# Appwrite: List subscribers

Retrieves a list of subscribers from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-list-subscribers?connectionId=$CONNECTION_ID&topicId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topicId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/messaging-list-subscribers?${params}`, {
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
| `topicId` | string | yes | Topic ID. The topic ID subscribed to. |
| `queries[]` | array<string> | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. You may filter on the following attributes: name, provider, type, enabled Accepts multiple values as an array. |
| `search` | string | no | Search term to filter your list results. Max length: 256 chars. |
| `total` | boolean | no | When set to false, the total count returned will be 0 and will not be calculated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscribers": [
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
| `subscribers` | array<object> | List of subscribers. |
| `total` | number | Total number of subscribers that matched your query. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /messaging/topics/{topicId}/subscribers` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/messaging-list-subscribers.md) for the provider-specific parameters and requirements.

