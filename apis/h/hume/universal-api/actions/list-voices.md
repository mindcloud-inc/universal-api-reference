# Hume: List voices



```
GET https://connect.mindcloud.co/v1/universal/hume/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hume/latest/actions/list-voices?connectionId=$CONNECTION_ID&limit=25&offset=0&provider=HUME_AI" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "provider": "HUME_AI"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hume/latest/actions/list-voices?${params}`, {
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
| `provider` | list | yes | Voice provider to list. HUME_AI returns shared Voice Library voices; CUSTOM_VOICE returns custom voices in the account. One of: `0`, `1`. Default: `HUME_AI`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ascendingOrder` | boolean | no | When true, returns voices in ascending order. |
| `filterTag` | string | no | Filter voices by tag using TAG:TAG_VALUE syntax, for example GENDER:Male. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": 1,
      "description": "string",
      "id": "string",
      "modifiedOn": 1,
      "name": "Ava Chen",
      "provider": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | number |  |
| `description` | string |  |
| `id` | string |  |
| `modifiedOn` | number |  |
| `name` | string |  |
| `provider` | string |  |

## Native endpoint

Through the native Hume API, this operation is `GET /v0/tts/voices` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

