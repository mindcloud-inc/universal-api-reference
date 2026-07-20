# Billit: Get Next Invoice Sequence

Retrieves the next Billit invoice sequence preview.

```
GET https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-next-invoice-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-next-invoice-sequence?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billit/latest/actions/get-next-invoice-sequence?${params}`, {
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
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Next Billit outgoing invoice sequence preview. |

## Native endpoint

Through the native Billit API, this operation is `POST /v1/account/sequences` (base URL `https://api.sandbox.billit.be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-next-invoice-sequence.md) for the provider-specific parameters and requirements.

