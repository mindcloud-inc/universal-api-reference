# MoneyBird: List Webhooks

Retrieves webhooks from MoneyBird.

```
GET https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoneyBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&administrationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "administrationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/list-webhooks?${params}`, {
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
| `administrationId` | string | yes | Moneybird administration ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administrationId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deactivatedAt": "2026-05-07T12:00:00.000Z",
      "enabledEvents": [
        "string"
      ],
      "id": "string",
      "lastHttpBody": "string",
      "lastHttpStatus": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrationId` | string |  |
| `createdAt` | date |  |
| `deactivatedAt` | date |  |
| `enabledEvents` | array<string> |  |
| `id` | string |  |
| `lastHttpBody` | string |  |
| `lastHttpStatus` | number |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native MoneyBird API, this operation is `GET /:administrationId/webhooks.json` (base URL `https://moneybird.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

