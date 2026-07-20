# Feedbin: Get Tagging

Retrieves a single tagging from Feedbin.

```
GET https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/get-tagging
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feedbin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/get-tagging?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/get-tagging?${params}`, {
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
| `id` | number | yes | Feedbin tagging ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "feed_id": 1,
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `feed_id` | number |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Feedbin API, this operation is `GET taggings/[:id].json` (base URL `https://api.feedbin.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tagging.md) for the provider-specific parameters and requirements.

