# MoreApp: Copy Form Version To Folder

Copies a form version to a folder in MoreApp.

```
PUT https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/copy-form-version-to-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/copy-form-version-to-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "formId": "string",
  "formVersionId": "string",
  "bodyCustomerId": 1,
  "folderId": "string",
  "formName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/copy-form-version-to-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "formId": "string",
    "formVersionId": "string",
    "bodyCustomerId": 1,
    "folderId": "string",
    "formName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes |  |
| `formId` | string | yes |  |
| `formVersionId` | string | yes |  |
| `brandingId` | string | no |  |
| `bodyCustomerId` | number | yes | Customer ID in the request body. |
| `folderId` | string | yes | Target folder ID for the copied form version. |
| `formName` | string | yes | Name for the copied form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder": {},
      "form": {},
      "formVersion": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder` | object | Target folder containing the copied form after the copy completes. |
| `form` | object | Copied form resource created by the operation. |
| `formVersion` | object | Draft form version created for the copied form. |

## Native endpoint

Through the native MoreApp API, this operation is `POST /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/{{formVersionId}}/copy` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-form-version-to-folder.md) for the provider-specific parameters and requirements.

