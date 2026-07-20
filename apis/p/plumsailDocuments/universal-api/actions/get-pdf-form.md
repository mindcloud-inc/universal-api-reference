# Plumsail Documents: Get PDF Form

Retrieves form fields from a PDF in Plumsail Documents.

```
GET https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/get-pdf-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plumsail Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/get-pdf-form?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/get-pdf-form?${params}`, {
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
| `password` | string | no |  |
| `file` | file | no |  |
| `fileUrl` | string | no |  |
| `callbackUrl` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Plumsail Documents API returns.

## Native endpoint

Through the native Plumsail Documents API, this operation is `GET /api/v2/pdf/get-form` (base URL `https://us-api.plumsail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pdf-form.md) for the provider-specific parameters and requirements.

