# Frappe: Get DocType Count V2

Retrieves the document count for a Frappe DocType.

```
GET https://connect.mindcloud.co/v1/universal/frappe/latest/actions/get-doctype-count-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frappe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frappe/latest/actions/get-doctype-count-v2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frappe/latest/actions/get-doctype-count-v2?${params}`, {
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
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Document count for the selected DocType. |

## Native endpoint

Through the native Frappe API, this operation is `GET /api/v2/doctype/{{arguments.doctype}}/count` (base URL `{{credentials.siteUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-doctype-count-v2.md) for the provider-specific parameters and requirements.

