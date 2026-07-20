# Spondyr: List Transaction Types

Retrieves transaction types from Spondyr.

```
GET https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/list-transaction-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spondyr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/list-transaction-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/list-transaction-types?${params}`, {
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
      "APIStatus": "string",
      "Data": [
        {}
      ],
      "ErrorMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `APIStatus` | string | Spondyr API execution status. |
| `Data` | array<object> | Transaction types returned by Spondyr. |
| `ErrorMessage` | string | Error details when the request fails. |

## Native endpoint

Through the native Spondyr API, this operation is `GET /TransactionTypes` (base URL `https://client.spondyr.io/api/v1.0.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transaction-types.md) for the provider-specific parameters and requirements.

