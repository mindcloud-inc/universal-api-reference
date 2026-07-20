# Qlik: Get Reload

Retrieves a reload from your Qlik tenant.

```
GET https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-reload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-reload?connectionId=$CONNECTION_ID&reloadId=67f6bd0f5a21e930bf7aee03" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reloadId": "67f6bd0f5a21e930bf7aee03"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-reload?${params}`, {
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
| `reloadId` | string | yes | Qlik reload ID. Example: `67f6bd0f5a21e930bf7aee03`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "endTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string",
      "tenantId": "string",
      "type": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `endTime` | date |  |
| `id` | string |  |
| `status` | string |  |
| `tenantId` | string |  |
| `type` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Qlik API, this operation is `GET /api/v1/reloads/:reloadId` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reload.md) for the provider-specific parameters and requirements.

