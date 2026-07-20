# Cloze: List Contact Segments

Retrieves contact segments from Cloze.

```
GET https://connect.mindcloud.co/v1/universal/cloze/latest/actions/list-contact-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloze/latest/actions/list-contact-segments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloze/latest/actions/list-contact-segments?${params}`, {
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
      "errorcode": 1,
      "list": [
        [
          {}
        ]
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorcode` | number | Error code. 0 means success |
| `list[]` | array<object> | Array of contact segments |
| `list[].key` | string | Internal segment key |
| `list[].name` | string | User label for the segment |
| `message` | string | If an error occurs, this is the human readable description |

## Native endpoint

Through the native Cloze API, this operation is `GET /v1/user/segments/people` (base URL `https://api.cloze.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-segments.md) for the provider-specific parameters and requirements.

