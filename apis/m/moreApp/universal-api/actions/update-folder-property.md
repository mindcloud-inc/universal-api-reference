# MoreApp: Update Folder Property

Updates a folder property in MoreApp.

```
PUT https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-folder-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-folder-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "folderId": "string",
  "[].op": "string",
  "[].path": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/update-folder-property', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "folderId": "string",
    "[].op": "string",
    "[].path": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes |  |
| `folderId` | string | yes |  |
| `[].op` | string | yes |  |
| `[].path` | string | yes |  |
| `[].value` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "forms": [
        {}
      ],
      "id": "string",
      "meta": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `forms` | array<object> |  |
| `id` | string |  |
| `meta` | object |  |
| `status` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `PATCH /api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-folder-property.md) for the provider-specific parameters and requirements.

