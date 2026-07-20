# PostcardMania: Get Balances

Retrieves account balances from PostcardMania.

```
GET https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/get-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/get-balances?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/get-balances?${params}`, {
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
      "customInventory": [
        {}
      ],
      "moneyOnAccount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customInventory` | array<object> | Custom inventory balances returned by PCM. |
| `moneyOnAccount` | number | Current money-on-account balance. |

## Native endpoint

Through the native PostcardMania API, this operation is `GET /integration/balance` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-balances.md) for the provider-specific parameters and requirements.

