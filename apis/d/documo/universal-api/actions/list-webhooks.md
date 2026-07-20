# Documo: List Webhooks

Retrieves webhook endpoint records from Documo.

```
GET https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-webhooks?${params}`, {
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
| `accountId` | string | no | Account UUID to filter webhooks. |
| `numberId` | string | no | Fax number UUID to filter webhooks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "rows": [
        {
          "attachmentEnabled": true,
          "authType": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "enabled": true,
          "name": "Ava Chen",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com",
          "uuid": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `rows[].attachmentEnabled` | boolean |  |
| `rows[].authType` | string |  |
| `rows[].createdAt` | date |  |
| `rows[].enabled` | boolean |  |
| `rows[].name` | string |  |
| `rows[].updatedAt` | date |  |
| `rows[].url` | string |  |
| `rows[].uuid` | string |  |

## Native endpoint

Through the native Documo API, this operation is `GET /webhooks` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

