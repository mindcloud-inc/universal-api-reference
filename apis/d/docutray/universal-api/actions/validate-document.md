# Docutray: Validate Document Type



```
GET https://connect.mindcloud.co/v1/universal/docutray/latest/actions/validate-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docutray `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/validate-document?connectionId=$CONNECTION_ID&id=string&document=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "document": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docutray/latest/actions/validate-document?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Document type ID |
| `document` | object | yes | JSON document to validate |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docutray API returns.

## Native endpoint

Through the native Docutray API, this operation is `POST api/document-types/:id/validate` (base URL `https://app.docutray.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-document.md) for the provider-specific parameters and requirements.

