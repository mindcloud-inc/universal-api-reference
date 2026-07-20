# Revel Digital: List Organizations



```
GET https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revel Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/list-organizations?${params}`, {
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
      "address_1": "string",
      "address_2": "string",
      "city": "string",
      "country": "string",
      "fax": "string",
      "id": "string",
      "language_code": "string",
      "name": "Ava Chen",
      "phone": "string",
      "postal_code": "string",
      "state": "string",
      "timeZone": "string",
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_1` | string |  |
| `address_2` | string |  |
| `city` | string |  |
| `country` | string |  |
| `fax` | string |  |
| `id` | string |  |
| `language_code` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `postal_code` | string |  |
| `state` | string |  |
| `timeZone` | string |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Revel Digital API, this operation is `GET /account/organizations` (base URL `https://api.reveldigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

