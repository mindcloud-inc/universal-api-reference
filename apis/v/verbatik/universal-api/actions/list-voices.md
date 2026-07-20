# Verbatik: List Voices

Retrieves a list of voices from Verbatik.

```
GET https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verbatik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/list-voices?${params}`, {
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
      "gender": "string",
      "id": "string",
      "is_neural": true,
      "language_code": "string",
      "language_name": "Ava Chen",
      "name": "Ava Chen",
      "sample_url": "https://example.com",
      "styles": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gender` | string |  |
| `id` | string |  |
| `is_neural` | boolean |  |
| `language_code` | string |  |
| `language_name` | string |  |
| `name` | string |  |
| `sample_url` | string |  |
| `styles[]` | array<string> |  |

## Native endpoint

Through the native Verbatik API, this operation is `GET /v1/voices` (base URL `https://api.verbatik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

