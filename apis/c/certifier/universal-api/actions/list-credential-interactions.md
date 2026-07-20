# Certifier: List Credential Interactions

Retrieves all credential interactions from Certifier.

```
GET https://connect.mindcloud.co/v1/universal/certifier/latest/actions/list-credential-interactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certifier `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/list-credential-interactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certifier/latest/actions/list-credential-interactions?${params}`, {
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
| `credentialId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credentialId": "string",
      "eventType": "string",
      "id": "string",
      "triggeredAt": "2026-05-07T12:00:00.000Z",
      "triggeredBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credentialId` | string |  |
| `eventType` | string |  |
| `id` | string |  |
| `triggeredAt` | date |  |
| `triggeredBy` | string |  |

## Native endpoint

Through the native Certifier API, this operation is `GET /credential-interactions` (base URL `https://api.certifier.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-credential-interactions.md) for the provider-specific parameters and requirements.

