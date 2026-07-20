# Podscan: Get Topic Demographics

Retrieves topic demographics data from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-topic-demographics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-topic-demographics?connectionId=$CONNECTION_ID&topicId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topicId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-topic-demographics?${params}`, {
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
| `topicId` | string | yes | The topic ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "podcasts": [
        {}
      ],
      "topic": {},
      "total_podcasts_with_demographics": 1,
      "total_podcasts_with_topic": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object |  |
| `podcasts` | array<object> |  |
| `topic` | object |  |
| `total_podcasts_with_demographics` | number |  |
| `total_podcasts_with_topic` | number |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /topics/{topicId}/demographics` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-topic-demographics.md) for the provider-specific parameters and requirements.

