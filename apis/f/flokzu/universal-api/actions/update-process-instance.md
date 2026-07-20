# Flokzu: Update Process Instance



```
PUT https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/update-process-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flokzu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/update-process-instance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/update-process-instance', {
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
      "identifier": "string",
      "status": "string",
      "updateDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `identifier` | string |  |
| `status` | string |  |
| `updateDate` | date |  |

## Native endpoint

Through the native Flokzu API, this operation is `PUT /v2/process/instance` (base URL `https://app.flokzu.com/flokzuopenapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-process-instance.md) for the provider-specific parameters and requirements.

