# Reteach: Get Customer Import



```
GET https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer-import
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reteach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer-import?connectionId=$CONNECTION_ID&customerImportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerImportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer-import?${params}`, {
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
| `customerImportId` | string | yes | The id of the customer import job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "string",
      "failedAt": "string",
      "failedCount": 1,
      "failedRows": [
        {}
      ],
      "id": "string",
      "isSendAcademyInvitationEnabled": true,
      "isTagSyncEnabled": true,
      "mode": "string",
      "originalFilename": "Ava Chen",
      "size": 1,
      "startedAt": "string",
      "successCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | string |  |
| `failedAt` | string |  |
| `failedCount` | number |  |
| `failedRows` | array<object> |  |
| `id` | string |  |
| `isSendAcademyInvitationEnabled` | boolean |  |
| `isTagSyncEnabled` | boolean |  |
| `mode` | string |  |
| `originalFilename` | string |  |
| `size` | number |  |
| `startedAt` | string |  |
| `successCount` | number |  |

## Native endpoint

Through the native Reteach API, this operation is `GET /customer-import/{customerImportId}` (base URL `https://api.reteach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-import.md) for the provider-specific parameters and requirements.

