# Eventee: Create Speaker

Creates a speaker in Eventee.

```
POST https://connect.mindcloud.co/v1/universal/eventee/latest/actions/create-speaker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/create-speaker" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventee/latest/actions/create-speaker', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "bio": "string",
      "company": "string",
      "country": "string",
      "email": "ava@example.com",
      "event_id": 1,
      "facebook": "string",
      "id": 1,
      "language": "string",
      "linkedIn": "https://example.com",
      "name": "Ava Chen",
      "phone": "string",
      "photo": "string",
      "position": "string",
      "thumbnail": "string",
      "twitter": "string",
      "web": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bio` | string |  |
| `company` | string |  |
| `country` | string |  |
| `email` | string |  |
| `event_id` | number |  |
| `facebook` | string |  |
| `id` | number |  |
| `language` | string |  |
| `linkedIn` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `photo` | string |  |
| `position` | string |  |
| `thumbnail` | string |  |
| `twitter` | string |  |
| `web` | string |  |

## Native endpoint

Through the native Eventee API, this operation is `POST /speaker` (base URL `https://api.eventee.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-speaker.md) for the provider-specific parameters and requirements.

