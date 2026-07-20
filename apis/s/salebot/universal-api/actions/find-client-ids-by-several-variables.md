# Salebot: Find Client IDs by Several Variables



```
GET https://connect.mindcloud.co/v1/universal/salebot/latest/actions/find-client-ids-by-several-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/find-client-ids-by-several-variables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salebot/latest/actions/find-client-ids-by-several-variables?${params}`, {
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
      "clientIds": [
        1
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientIds` | array<number> |  |
| `status` | string |  |

## Native endpoint

Through the native Salebot API, this operation is `GET /find_all_client_id_by_several_vars` (base URL `https://chatter.salebot.pro/api/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-client-ids-by-several-variables.md) for the provider-specific parameters and requirements.

