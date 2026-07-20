# Middesk: Prefill business information

Prefills business information in your Middesk account.

```
POST https://connect.mindcloud.co/v1/universal/middesk/latest/actions/business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/business" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/middesk/latest/actions/business', {
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
      "addresses": [
        {}
      ],
      "formation": {},
      "industryClassifications": [
        {}
      ],
      "names": [
        {}
      ],
      "object": "string",
      "people": [
        {}
      ],
      "tin": {},
      "website": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `formation` | object |  |
| `industryClassifications` | array<object> |  |
| `names` | array<object> |  |
| `object` | string |  |
| `people` | array<object> |  |
| `tin` | object |  |
| `website` | object |  |

## Native endpoint

Through the native Middesk API, this operation is `POST /prefill/businesses` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/business.md) for the provider-specific parameters and requirements.

