# AbcSubmit: Get Form Document

Retrieves a form document from AbcSubmit.

```
GET https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-form-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AbcSubmit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-form-document?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-form-document?${params}`, {
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
| `formId` | string | yes | The ID of the form document to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AbcSubmit API returns.

## Native endpoint

Through the native AbcSubmit API, this operation is `GET /api/v1/forms/:form_id` (base URL `https://www.abcsubmit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-document.md) for the provider-specific parameters and requirements.

