# Envoice: List Tax Rates

Retrieves tax rates from Envoice.

```
GET https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-tax-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-tax-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-tax-rates?${params}`, {
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
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "Id": 1,
      "Name": "Ava Chen",
      "Percentage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreatedOn` | date | Tax rate creation timestamp. |
| `Id` | number | Tax rate identifier. |
| `Name` | string | Tax rate name. |
| `Percentage` | number | Tax rate percentage. |

## Native endpoint

Through the native Envoice API, this operation is `GET tax/all` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tax-rates.md) for the provider-specific parameters and requirements.

