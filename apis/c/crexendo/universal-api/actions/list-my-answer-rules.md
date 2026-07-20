# Crexendo: List My Answer Rules

Retrieves your answer rules from Crexendo.

```
GET https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-my-answer-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crexendo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-my-answer-rules?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-my-answer-rules?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "enabled": "string",
      "is-active": true,
      "order": 1,
      "time-frame": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `enabled` | string |  |
| `is-active` | boolean |  |
| `order` | number |  |
| `time-frame` | string |  |
| `user` | string |  |

## Native endpoint

Through the native Crexendo API, this operation is `GET /domains/~/users/~/answerrules` (base URL `https://ns-api.com/ns-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-my-answer-rules.md) for the provider-specific parameters and requirements.

