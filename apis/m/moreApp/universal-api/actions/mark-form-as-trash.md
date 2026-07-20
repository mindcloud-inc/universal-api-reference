# MoreApp: Mark Form As Trash

Marks a form as trash in MoreApp.

```
DELETE https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/mark-form-as-trash
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/mark-form-as-trash?connectionId=$CONNECTION_ID&customerId=1&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/mark-form-as-trash?${params}`, {
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
| `customerId` | number | yes |  |
| `formId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "meta": {},
      "publishedVersion": {},
      "scope": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `meta` | object |  |
| `publishedVersion` | object |  |
| `scope` | string |  |
| `status` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `DELETE /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-form-as-trash.md) for the provider-specific parameters and requirements.

