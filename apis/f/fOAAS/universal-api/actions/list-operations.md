# FOAAS: List Operations



```
GET https://connect.mindcloud.co/v1/universal/fOAAS/latest/actions/list-operations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FOAAS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fOAAS/latest/actions/list-operations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fOAAS/latest/actions/list-operations?${params}`, {
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
      "": [
        {
          "fields": [
            {
              "field": "string",
              "name": "Ava Chen"
            }
          ],
          "name": "Ava Chen",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[]` | array<object> |  |
| `[].fields` | array<object> |  |
| `[].fields[].field` | string |  |
| `[].fields[].name` | string |  |
| `[].name` | string |  |
| `[].url` | string |  |

## Native endpoint

Through the native FOAAS API, this operation is `GET /operations` (base URL `https://foaas.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-operations.md) for the provider-specific parameters and requirements.

