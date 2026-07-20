# OKSign: Update Organization Token Info

Updates organization token info in OKSign.

```
PUT https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/update-organization-token-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OKSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/update-organization-token-info" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/update-organization-token-info', {
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
      "reason": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reason` | array<string> | Validation errors when the update fails. |
| `status` | string |  |

## Native endpoint

Through the native OKSign API, this operation is `POST /orgtokeninfo/update` (base URL `https://www.oksign.be/services/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization-token-info.md) for the provider-specific parameters and requirements.

