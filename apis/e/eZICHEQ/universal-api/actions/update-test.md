# EZICHEQ: Update Test



```
PUT https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/update-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZICHEQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/update-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/update-test', {
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
      "count": 1,
      "date": "string",
      "error": "string",
      "request_method": "string",
      "request_uri": "string",
      "results": {},
      "status": "string",
      "status_code": 1,
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `date` | string |  |
| `error` | string |  |
| `request_method` | string |  |
| `request_uri` | string |  |
| `results` | object |  |
| `status` | string |  |
| `status_code` | number |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native EZICHEQ API, this operation is `PUT /test` (base URL `https://api.ezicheq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-test.md) for the provider-specific parameters and requirements.

