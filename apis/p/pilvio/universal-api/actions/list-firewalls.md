# Pilvio: List Firewalls



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-firewalls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-firewalls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-firewalls?${params}`, {
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
      "billingAccountId": 1,
      "description": "string",
      "name": "Ava Chen",
      "rules": [
        {
          "uuid": "string"
        }
      ],
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAccountId` | number |  |
| `description` | string |  |
| `name` | string |  |
| `rules[].uuid` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /network/firewalls` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-firewalls.md) for the provider-specific parameters and requirements.

