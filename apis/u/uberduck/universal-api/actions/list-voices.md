# Uberduck: List Voices

Retrieves available voice options from Uberduck.

```
GET https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uberduck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/list-voices?${params}`, {
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
| `age` | string | no | Filter voices by age. |
| `gender` | string | no | Filter voices by gender. |
| `accent` | string | no | Filter voices by accent. |
| `mood` | string | no | Filter voices by mood. |
| `style` | string | no | Filter voices by style. |
| `language` | string | no | Filter voices by language. |
| `limit` | number | no | Maximum number of voices to return. |
| `offset` | number | no | Number of voices to skip. |
| `private` | boolean | no | Whether to include private voices. |
| `name` | string | no | Filter voices by name. |
| `uuid` | string | no | Filter voices by voice UUID. |
| `model` | string | no | Filter voices by model ID. |
| `tag` | string | no | Filter voices by tag. |
| `searchTerm` | string | no | Keyword search across voice name and display name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "total": 1,
      "voices": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total` | number | Total number of voices matching the filter. |
| `voices` | array<object> | List of matching voices. |

## Native endpoint

Through the native Uberduck API, this operation is `GET /v1/voices` (base URL `https://api.uberduck.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

