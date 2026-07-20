# RemOnline: List Estimate Statuses

Retrieves a list of estimate statuses from RemOnline.

```
GET https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/list-estimate-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RemOnline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/list-estimate-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/list-estimate-statuses?${params}`, {
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
      "color": "string",
      "group": {
        "name": "Ava Chen",
        "type": 1
      },
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `group.name` | string |  |
| `group.type` | number |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native RemOnline API, this operation is `GET /estimates/statuses` (base URL `https://api.roapp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-estimate-statuses.md) for the provider-specific parameters and requirements.

