# GoCanvas: Retrieve Form



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-form?connectionId=$CONNECTION_ID&formId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-form?${params}`, {
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
| `formId` | number | yes |  |
| `format` | list | no | The response format. Defaults to nested. One of: `flat`, `metadata`, `minimal`, `nested`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "builderType": "string",
      "builderVersion": "string",
      "dispatchEnabled": true,
      "emailOptions": 1,
      "id": 1,
      "imageId": 1,
      "isLockedByCanvas": true,
      "mobileBuilderEnabled": true,
      "name": "Ava Chen",
      "rootVersionId": 1,
      "rootVersionUpdatedAt": "string",
      "sheetStyleEnabled": true,
      "status": "string",
      "type": "string",
      "updatedAt": "string",
      "version": 1,
      "viewPdfMobile": true,
      "webForm": true,
      "workflowEnabled": true,
      "workflowId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `builderType` | string |  |
| `builderVersion` | string |  |
| `dispatchEnabled` | boolean |  |
| `emailOptions` | number |  |
| `id` | number |  |
| `imageId` | number |  |
| `isLockedByCanvas` | boolean |  |
| `mobileBuilderEnabled` | boolean |  |
| `name` | string |  |
| `rootVersionId` | number |  |
| `rootVersionUpdatedAt` | string |  |
| `sheetStyleEnabled` | boolean |  |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `version` | number |  |
| `viewPdfMobile` | boolean |  |
| `webForm` | boolean |  |
| `workflowEnabled` | boolean |  |
| `workflowId` | number |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /forms/:formId` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-form.md) for the provider-specific parameters and requirements.

