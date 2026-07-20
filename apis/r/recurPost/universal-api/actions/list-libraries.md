# RecurPost: List Libraries

Retrieves content libraries from RecurPost.

```
GET https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/list-libraries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RecurPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/list-libraries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/list-libraries?${params}`, {
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
      "library_list": [
        {}
      ],
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `library_list` | array<object> |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native RecurPost API, this operation is `POST /api/library_list` (base URL `https://social.recurpost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-libraries.md) for the provider-specific parameters and requirements.

