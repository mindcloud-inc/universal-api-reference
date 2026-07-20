# Curator: List Ads

Retrieves ads and custom posts from Curator.

```
GET https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-ads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Curator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-ads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-ads?${params}`, {
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
| `feedId` | string | no | Optional feed filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clickAction": "string",
      "feedId": "string",
      "id": "string",
      "name": "Ava Chen",
      "networkId": 1,
      "networkName": "Ava Chen",
      "positionRepeatInterval": 1,
      "positionRepeats": true,
      "positionStart": 1,
      "slug": "string",
      "status": "string",
      "text": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clickAction` | string |  |
| `feedId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `networkId` | number |  |
| `networkName` | string |  |
| `positionRepeatInterval` | number |  |
| `positionRepeats` | boolean |  |
| `positionStart` | number |  |
| `slug` | string |  |
| `status` | string |  |
| `text` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Curator API, this operation is `GET /v1.2/ads` (base URL `https://api.curator.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ads.md) for the provider-specific parameters and requirements.

