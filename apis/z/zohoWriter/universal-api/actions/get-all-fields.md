# Zoho Writer: Get All Fields

Retrieves all fields from a Zoho Writer document.

```
GET https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/get-all-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Writer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/get-all-fields?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/get-all-fields?${params}`, {
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
| `documentId` | string | yes | The unique ID of the Zoho Writer document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fill": [
        {}
      ],
      "merge": [
        {}
      ],
      "sign": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fill` | array<object> |  |
| `merge` | array<object> |  |
| `sign` | object |  |

## Native endpoint

Through the native Zoho Writer API, this operation is `GET /v1/documents/:document_id/fields` (base URL `{{credentials.accessTokenRequest.api_domain}}/writer/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-fields.md) for the provider-specific parameters and requirements.

