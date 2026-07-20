# Frappe: List Documents V2

Lists documents from a Frappe DocType.

```
GET https://connect.mindcloud.co/v1/universal/frappe/latest/actions/list-documents-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frappe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frappe/latest/actions/list-documents-v2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frappe/latest/actions/list-documents-v2?${params}`, {
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
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of documents returned for the selected DocType. |

## Native endpoint

Through the native Frappe API, this operation is `GET /api/v2/document/{{arguments.doctype}}` (base URL `{{credentials.siteUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents-v2.md) for the provider-specific parameters and requirements.

