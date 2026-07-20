# Moaform: List Webhooks

Retrieves webhooks for a form in Moaform.

```
GET https://connect.mindcloud.co/v1/universal/moaform/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moaform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moaform/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moaform/latest/actions/list-webhooks?${params}`, {
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
| `formId` | string | yes | Unique ID of the form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "enabled": true,
          "endpoint": "string",
          "id": "string",
          "retentionDays": 1,
          "secret": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "verifySsl": true
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
| `items` | array<object> |  |
| `items[].createdAt` | date |  |
| `items[].enabled` | boolean |  |
| `items[].endpoint` | string |  |
| `items[].id` | string |  |
| `items[].retentionDays` | number |  |
| `items[].secret` | string |  |
| `items[].updatedAt` | date |  |
| `items[].verifySsl` | boolean |  |

## Native endpoint

Through the native Moaform API, this operation is `GET /forms/:formId/webhooks` (base URL `https://api.moaform.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

