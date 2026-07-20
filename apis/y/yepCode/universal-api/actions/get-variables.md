# YepCode: Get variables

Retrieves a list of variables from YepCode.

```
GET https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-variables?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-variables?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "id": "string",
      "isSensitive": true,
      "key": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Timestamp when the variable was created |
| `createdBy` | string | Username of the user who created the variable |
| `id` | string | Unique identifier (UUID) of the team variable |
| `isSensitive` | boolean | Whether the variable is marked as sensitive |
| `key` | string | Variable key used in processes |
| `value` | string | Variable value |

## Native endpoint

Through the native YepCode API, this operation is `GET /variables` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-variables.md) for the provider-specific parameters and requirements.

