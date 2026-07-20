# BoxHero: Get Linked Team

Retrieves the linked team from BoxHero.

```
GET https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-linked-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoxHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-linked-team?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-linked-team?${params}`, {
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
      "currency_symbol": "string",
      "id": 1,
      "memo": "string",
      "mode": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency_symbol` | string |  |
| `id` | number |  |
| `memo` | string |  |
| `mode` | number |  |
| `name` | string |  |

## Native endpoint

Through the native BoxHero API, this operation is `GET /v1/teams/linked` (base URL `https://rest.boxhero-app.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-linked-team.md) for the provider-specific parameters and requirements.

