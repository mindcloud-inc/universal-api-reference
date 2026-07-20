# SuperSend: List Announcements

Retrieves announcements from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-announcements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-announcements?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-announcements?${params}`, {
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
      "announcements": [
        {
          "id": "string",
          "link": "https://example.com",
          "message": "string",
          "severity": "string",
          "source": "string",
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `announcements[].id` | string |  |
| `announcements[].link` | string |  |
| `announcements[].message` | string |  |
| `announcements[].severity` | string |  |
| `announcements[].source` | string |  |
| `announcements[].title` | string |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /announcements` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-announcements.md) for the provider-specific parameters and requirements.

