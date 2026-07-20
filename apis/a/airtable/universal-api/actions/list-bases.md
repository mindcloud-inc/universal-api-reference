# Airtable: List Bases

Retrieves accessible bases from the Airtable account.

```
GET https://connect.mindcloud.co/v1/universal/airtable/latest/actions/list-bases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airtable/latest/actions/list-bases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airtable/latest/actions/list-bases?${params}`, {
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
      "permissionLevel": "string"
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
| `permissionLevel` | string |  |

## Native endpoint

Through the native Airtable API, this operation is `GET /meta/bases` (base URL `https://api.airtable.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bases.md) for the provider-specific parameters and requirements.

