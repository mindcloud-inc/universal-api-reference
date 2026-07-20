# Checkmk: List Service Groups

Retrieves service group records from Checkmk.

```
GET https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/list-service-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkmk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/list-service-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/list-service-groups?${params}`, {
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
      "extensions": {},
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extensions` | object |  |
| `id` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Checkmk API, this operation is `GET /domain-types/service_group_config/collections/all` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-groups.md) for the provider-specific parameters and requirements.

