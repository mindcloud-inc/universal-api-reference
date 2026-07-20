# Slashdot: Get Ask Slashdot Feed

Retrieves the Ask Slashdot feed.

```
GET https://connect.mindcloud.co/v1/universal/slashdot/latest/actions/get-ask-slashdot-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slashdot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slashdot/latest/actions/get-ask-slashdot-feed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slashdot/latest/actions/get-ask-slashdot-feed?${params}`, {
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
      "dc:creator": "string",
      "dc:date": "2026-05-07T12:00:00.000Z",
      "dc:subject": "string",
      "description": "string",
      "link": "https://example.com",
      "slash:comments": "string",
      "slash:department": "string",
      "slash:hit_parade": "string",
      "slash:section": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dc:creator` | string |  |
| `dc:date` | date |  |
| `dc:subject` | string |  |
| `description` | string |  |
| `link` | string |  |
| `slash:comments` | string |  |
| `slash:department` | string |  |
| `slash:hit_parade` | string |  |
| `slash:section` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Slashdot API, this operation is `GET slashdotAskSlashdot` (base URL `https://rss.slashdot.org/Slashdot/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ask-slashdot-feed.md) for the provider-specific parameters and requirements.

