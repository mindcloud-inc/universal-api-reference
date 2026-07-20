# Reka Vision: Quick Tag (V1)

Creates metadata tags for short videos in Reka Vision.

```
POST https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/quick-tag-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/quick-tag-v1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/quick-tag-v1', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "video": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `video` | file | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adultcontent": true,
      "alcohol": true,
      "description": "string",
      "drugs": true,
      "expectedctr": 1,
      "gambling": true,
      "keyword": [
        "string"
      ],
      "moodtone": [
        "string"
      ],
      "political": true,
      "profanity": true,
      "violence": true,
      "viralityscore": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adultcontent` | boolean |  |
| `alcohol` | boolean |  |
| `description` | string |  |
| `drugs` | boolean |  |
| `expectedctr` | number |  |
| `gambling` | boolean |  |
| `keyword` | array<string> |  |
| `moodtone` | array<string> |  |
| `political` | boolean |  |
| `profanity` | boolean |  |
| `violence` | boolean |  |
| `viralityscore` | number |  |

## Native endpoint

Through the native Reka Vision API, this operation is `POST /v1/qa/quicktag` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/quick-tag-v1.md) for the provider-specific parameters and requirements.

