# AbcSubmit: Get Form Template Document

Retrieves a form template document from AbcSubmit.

```
GET https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-form-template-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AbcSubmit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-form-template-document?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-form-template-document?${params}`, {
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
| `formId` | string | yes | The ID of the form template document to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AbcSubmit API returns.

## Native endpoint

Through the native AbcSubmit API, this operation is `GET /api/v1/templates/:form_id` (base URL `https://www.abcsubmit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-template-document.md) for the provider-specific parameters and requirements.

