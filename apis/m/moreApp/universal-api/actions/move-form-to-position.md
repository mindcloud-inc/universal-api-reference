# MoreApp: Move Form To Position

Moves a form to a folder position in MoreApp.

```
PUT https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/move-form-to-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/move-form-to-position" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "folderId": "string",
  "formId": "string",
  "position": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/move-form-to-position', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "folderId": "string",
    "formId": "string",
    "position": 1
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
| `formId` | string | yes |  |
| `position` | number | yes |  |

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
| `forms` | array<object> | Folder forms after the move operation. |
| `id` | string | Folder identifier returned after the form is repositioned. |
| `meta` | object | Folder metadata after the move operation. |
| `status` | string | Folder status after the move operation. |

## Native endpoint

Through the native MoreApp API, this operation is `PUT /api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}/forms/{{formId}}/move/{{position}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-form-to-position.md) for the provider-specific parameters and requirements.

