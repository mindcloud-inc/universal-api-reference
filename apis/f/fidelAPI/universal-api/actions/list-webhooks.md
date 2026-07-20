# Fidel API: List Webhooks

Retrieves webhooks from a Fidel program.

```
GET https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&programId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "programId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-webhooks?${params}`, {
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
| `programId` | string | yes |  |
| `event` | string | no | Filter webhooks by event name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "event": "string",
      "id": "string",
      "live": true,
      "programId": "string",
      "secretKey": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `created` | date |  |
| `event` | string |  |
| `id` | string |  |
| `live` | boolean |  |
| `programId` | string |  |
| `secretKey` | string |  |
| `updated` | date |  |
| `url` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Fidel API API, this operation is `GET /programs/:programId/hooks` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

