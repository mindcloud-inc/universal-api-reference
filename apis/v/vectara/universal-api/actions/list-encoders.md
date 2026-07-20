# Vectara: List Encoders

Retrieves the available encoders from Vectara.

```
GET https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-encoders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-encoders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-encoders?${params}`, {
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
| `filter` | string | no | Regex filter against encoder names and descriptions. |
| `limit` | number | no | Maximum number of encoders to return. |
| `pageKey` | string | no | Cursor for the next page of encoders. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "encoders": [
        {}
      ],
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `encoders` | array<object> | List of encoders. |
| `metadata` | object | Pagination metadata for the list response. |

## Native endpoint

Through the native Vectara API, this operation is `GET /v2/encoders` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-encoders.md) for the provider-specific parameters and requirements.

