# Frappe: Run Document Method V2 (GET)

Runs a method on a Frappe document with GET.

```
GET https://connect.mindcloud.co/v1/universal/frappe/latest/actions/run-document-method-v2-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frappe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frappe/latest/actions/run-document-method-v2-get?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frappe/latest/actions/run-document-method-v2-get?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Frappe API returns.

## Native endpoint

Through the native Frappe API, this operation is `GET /api/v2/document/{{arguments.doctype}}/{{arguments.documentName}}/method/{{arguments.methodName}}` (base URL `{{credentials.siteUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-document-method-v2-get.md) for the provider-specific parameters and requirements.

