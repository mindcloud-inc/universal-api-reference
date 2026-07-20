# Zahara: List Currencies

Retrieves available currencies from the Zahara tenancy.

```
GET https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-currencies?${params}`, {
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
      "CurrencyId": 1,
      "IsActive": true,
      "LastUpdated": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "ShortName": "Ava Chen",
      "Symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CurrencyId` | number | Currency ID. |
| `IsActive` | boolean | Whether the currency is active. |
| `LastUpdated` | date | Last update timestamp. |
| `Name` | string | Currency name. |
| `ShortName` | string | Currency short code. |
| `Symbol` | string | Currency symbol. |

## Native endpoint

Through the native Zahara API, this operation is `GET /api/{{credentials.tenancyApiKey}}/Currencies` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-currencies.md) for the provider-specific parameters and requirements.

