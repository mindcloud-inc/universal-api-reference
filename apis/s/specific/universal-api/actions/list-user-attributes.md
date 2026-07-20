# Specific: List User Attributes

Retrieves user custom fields from Specific.

```
GET https://connect.mindcloud.co/v1/universal/specific/latest/actions/list-user-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Specific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/specific/latest/actions/list-user-attributes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/specific/latest/actions/list-user-attributes?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Specific API, this operation is `POST` (base URL `https://public-api.specific.app/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-attributes.md) for the provider-specific parameters and requirements.

