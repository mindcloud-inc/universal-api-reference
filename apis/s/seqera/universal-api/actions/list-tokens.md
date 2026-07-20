# Seqera: List Tokens

Retrieves API access tokens from Seqera.

```
GET https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-tokens?${params}`, {
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
      "tokens": [
        {
          "basicAuth": "string",
          "dateCreated": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "lastUsed": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "token": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tokens` | array<object> | Personal access tokens visible to the authenticated user. |
| `tokens[].basicAuth` | string | Basic auth marker, when present. |
| `tokens[].dateCreated` | date | Timestamp when the token was created. |
| `tokens[].id` | number | Token ID. |
| `tokens[].lastUsed` | date | Timestamp of last token use. |
| `tokens[].name` | string | Token name. |
| `tokens[].token` | string | Token secret value, when returned by the provider. |

## Native endpoint

Through the native Seqera API, this operation is `GET /tokens` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tokens.md) for the provider-specific parameters and requirements.

