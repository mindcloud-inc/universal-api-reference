# Frappe: Create Document V2

Creates a new document in a Frappe DocType.

```
POST https://connect.mindcloud.co/v1/universal/frappe/latest/actions/create-document-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frappe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frappe/latest/actions/create-document-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frappe/latest/actions/create-document-v2', {
  method: 'POST',
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
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | The document created in Frappe. |

## Native endpoint

Through the native Frappe API, this operation is `POST /api/v2/document/{{arguments.doctype}}` (base URL `{{credentials.siteUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-v2.md) for the provider-specific parameters and requirements.

