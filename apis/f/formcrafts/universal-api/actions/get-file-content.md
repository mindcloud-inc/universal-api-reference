# Formcrafts: Get File Content

Retrieves the content of an uploaded file from Formcrafts.

```
GET https://connect.mindcloud.co/v1/universal/formcrafts/latest/actions/get-file-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formcrafts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formcrafts/latest/actions/get-file-content?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formcrafts/latest/actions/get-file-content?${params}`, {
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
| `id` | string | yes | The Formcrafts file ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Formcrafts API returns.

## Native endpoint

Through the native Formcrafts API, this operation is `GET /files/:id/content` (base URL `https://api.formcrafts.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-content.md) for the provider-specific parameters and requirements.

