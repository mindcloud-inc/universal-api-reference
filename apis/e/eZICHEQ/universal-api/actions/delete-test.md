# EZICHEQ: Delete Test



```
DELETE https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/delete-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZICHEQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/delete-test?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eZICHEQ/latest/actions/delete-test?${params}`, {
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

Through the native EZICHEQ API, this operation is `DELETE /test` (base URL `https://api.ezicheq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-test.md) for the provider-specific parameters and requirements.

