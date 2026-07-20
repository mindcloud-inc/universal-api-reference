# Ortto: List Tags



```
GET https://connect.mindcloud.co/v1/universal/ortto/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ortto/latest/actions/list-tags?${params}`, {
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
| `q` | string | no | Search tag names. Ortto splits the value into tokens and matches all tokens. Default: ` `. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "createdAt": "string",
      "createdByEmail": "ava@example.com",
      "createdById": "string",
      "createdByName": "Ava Chen",
      "id": 1,
      "instanceId": "string",
      "lastUsed": "string",
      "name": "Ava Chen",
      "subscribers": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `createdAt` | string |  |
| `createdByEmail` | string |  |
| `createdById` | string |  |
| `createdByName` | string |  |
| `id` | number |  |
| `instanceId` | string |  |
| `lastUsed` | string |  |
| `name` | string |  |
| `subscribers` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Ortto API, this operation is `POST /tags/get` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

