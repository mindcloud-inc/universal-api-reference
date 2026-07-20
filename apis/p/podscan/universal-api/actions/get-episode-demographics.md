# Podscan: Get Episode Demographics

Retrieves episode demographics data from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-episode-demographics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-episode-demographics?connectionId=$CONNECTION_ID&episode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "episode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-episode-demographics?${params}`, {
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
| `episode` | string | yes | The episode ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "demographics": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `demographics` | object |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /episodes/{episode}/demographics` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-episode-demographics.md) for the provider-specific parameters and requirements.

