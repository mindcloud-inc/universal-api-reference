# Smoove: List Contact Fields

Retrieves contact field definitions from Smoove.

```
GET https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-contact-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smoove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-contact-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smoove/latest/actions/list-contact-fields?${params}`, {
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
      "custom": true,
      "key": "string",
      "label": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom` | boolean |  |
| `key` | string |  |
| `label` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Smoove API, this operation is `GET /v1/Account/ContactFields` (base URL `https://rest.smoove.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-fields.md) for the provider-specific parameters and requirements.

