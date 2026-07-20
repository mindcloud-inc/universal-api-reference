# Beds24: List Properties

Retrieves properties from Beds24.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-properties-2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-properties-2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-properties-2?${params}`, {
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
      "account": 1,
      "address": "string",
      "city": "string",
      "currency": "string",
      "id": 1,
      "name": "Ava Chen",
      "propertyType": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | number | Beds24 account ID owning the property. |
| `address` | string | Property street address. |
| `city` | string | Property city. |
| `currency` | string | Property currency. |
| `id` | number | Beds24 property ID. |
| `name` | string | Property name. |
| `propertyType` | string | Beds24 property type. |
| `state` | string | Property state or region. |

## Native endpoint

Through the native Beds24 API, this operation is `GET /properties` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-properties-2.md) for the provider-specific parameters and requirements.

