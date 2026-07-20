# Uspacy: List Outgoing Webhooks

Retrieves outgoing webhook entries from Uspacy.

```
GET https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/list-outgoing-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uspacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/list-outgoing-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/list-outgoing-webhooks?${params}`, {
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
      "data": [
        {}
      ],
      "links": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `links` | object |  |
| `meta` | object |  |

## Native endpoint

Through the native Uspacy API, this operation is `GET /company/v1/webhooks` (base URL `https://{{credentials.site}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-outgoing-webhooks.md) for the provider-specific parameters and requirements.

