# eWeLink: Add Home

Creates a new home in eWeLink.

```
POST https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/add-home
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/add-home" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/add-home', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "index": 1,
      "name": "Ava Chen",
      "roomList": [
        {
          "id": "string",
          "index": 1,
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `index` | number |  |
| `name` | string |  |
| `roomList[].id` | string |  |
| `roomList[].index` | number |  |
| `roomList[].name` | string |  |

## Native endpoint

Through the native eWeLink API, this operation is `POST /v2/family` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-home.md) for the provider-specific parameters and requirements.

