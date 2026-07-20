# Frappe: Run Document Method V2 (POST)

Runs a method on a Frappe document with POST.

```
PUT https://connect.mindcloud.co/v1/universal/frappe/latest/actions/run-document-method-v2-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frappe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frappe/latest/actions/run-document-method-v2-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frappe/latest/actions/run-document-method-v2-post', {
  method: 'PUT',
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Frappe API returns.

## Native endpoint

Through the native Frappe API, this operation is `POST /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/method/{{arguments.methodName}}` (base URL `{{credentials.siteUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-document-method-v2-post.md) for the provider-specific parameters and requirements.

