# WeBeHome: Save Action Set Show In Main



```
PUT https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/save-action-set-show-in-main
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeBeHome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/save-action-set-show-in-main" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/save-action-set-show-in-main', {
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
      "Created": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Created` | string |  |

## Native endpoint

Through the native WeBeHome API, this operation is `POST OpenAPIservice.svc/ActionSet/SaveShowInMain` (base URL `https://webehome.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-action-set-show-in-main.md) for the provider-specific parameters and requirements.

