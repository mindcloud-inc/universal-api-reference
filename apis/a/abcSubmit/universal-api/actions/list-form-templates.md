# AbcSubmit: List Form Templates

Retrieves form templates from AbcSubmit.

```
GET https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/list-form-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AbcSubmit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/list-form-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/list-form-templates?${params}`, {
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
      "createdDate": "2026-05-07T12:00:00.000Z",
      "document": "string",
      "docVersion": "string",
      "id": "string",
      "isTemplate": true,
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | date |  |
| `document` | string |  |
| `docVersion` | string |  |
| `id` | string |  |
| `isTemplate` | boolean |  |
| `lastUpdated` | date |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native AbcSubmit API, this operation is `GET /api/v1/templates` (base URL `https://www.abcsubmit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-templates.md) for the provider-specific parameters and requirements.

