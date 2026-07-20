# Memento Database: List Libraries

Retrieves all libraries from Memento Database.

```
GET https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/list-libraries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memento Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/list-libraries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/list-libraries?${params}`, {
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
      "libraries": [
        {}
      ],
      "nextPageToken": "string",
      "revision": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `libraries` | array<object> |  |
| `nextPageToken` | string |  |
| `revision` | number |  |

## Native endpoint

Through the native Memento Database API, this operation is `GET /libraries` (base URL `https://api.mementodatabase.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-libraries.md) for the provider-specific parameters and requirements.

