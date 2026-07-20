# Famulor AI - Voice Agent: List Assistants

Retrieves assistants from Famulor.

```
GET https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/list-assistants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Famulor AI - Voice Agent `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/list-assistants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/list-assistants?${params}`, {
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
      "current_page": 1,
      "data": [
        {}
      ],
      "per_page": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number | Current result page. |
| `data` | array<object> | Assistant records. |
| `per_page` | number | Assistants per page. |
| `total` | number | Total assistants. |

## Native endpoint

Through the native Famulor AI - Voice Agent API, this operation is `GET /user/assistants/get` (base URL `https://app.famulor.de/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assistants.md) for the provider-specific parameters and requirements.

