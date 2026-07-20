# PDF Snake: Get Byte Balance

Retrieves your current byte balance from PDF Snake.

```
GET https://connect.mindcloud.co/v1/universal/pDFSnake/latest/actions/get-byte-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Snake `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFSnake/latest/actions/get-byte-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFSnake/latest/actions/get-byte-balance?${params}`, {
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
      "balance": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number | Current remaining PDF Snake byte balance. |

## Native endpoint

Through the native PDF Snake API, this operation is `POST /balance` (base URL `https://api2.pdfsnake.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-byte-balance.md) for the provider-specific parameters and requirements.

