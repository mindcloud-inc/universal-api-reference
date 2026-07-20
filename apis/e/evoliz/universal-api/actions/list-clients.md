# Evoliz: List Clients

Retrieves clients from Evoliz.

```
GET https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evoliz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/list-clients?${params}`, {
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
      "address": {
        "country": {
          "iso2": "string",
          "label": "string"
        },
        "postcode": "string",
        "town": "string"
      },
      "clientid": 1,
      "code": "string",
      "comment": "string",
      "enabled": true,
      "name": "Ava Chen",
      "phone": "string",
      "safe_amount": 1,
      "stampdate": "2026-05-07T12:00:00.000Z",
      "ttc": true,
      "type": "string",
      "userid": 1,
      "vat_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.country.iso2` | string |  |
| `address.country.label` | string |  |
| `address.postcode` | string |  |
| `address.town` | string |  |
| `clientid` | number |  |
| `code` | string |  |
| `comment` | string |  |
| `enabled` | boolean |  |
| `name` | string |  |
| `phone` | string |  |
| `safe_amount` | number |  |
| `stampdate` | date |  |
| `ttc` | boolean |  |
| `type` | string |  |
| `userid` | number |  |
| `vat_number` | string |  |

## Native endpoint

Through the native Evoliz API, this operation is `GET /api/v1/clients` (base URL `https://www.evoliz.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

