# Scoro: List Event Resources

Retrieves event resources from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-event-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-event-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-event-resources?${params}`, {
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
      "modified_date": "string",
      "resource_color": "string",
      "resource_id": 1,
      "resource_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `modified_date` | string |  |
| `resource_color` | string |  |
| `resource_id` | number |  |
| `resource_name` | string |  |

## Native endpoint

Through the native Scoro API, this operation is `POST eventsResources/list` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-resources.md) for the provider-specific parameters and requirements.

