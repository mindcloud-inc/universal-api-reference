# JotUrl: Update Domain

Updates an existing domain in JotUrl.

```
PUT https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/update-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JotUrl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/update-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/update-domain', {
  method: 'PUT',
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
      "result": {},
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `status` | object |  |

## Native endpoint

Through the native JotUrl API, this operation is `POST /domains/edit` (base URL `https://joturl.com/a/i1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-domain.md) for the provider-specific parameters and requirements.

