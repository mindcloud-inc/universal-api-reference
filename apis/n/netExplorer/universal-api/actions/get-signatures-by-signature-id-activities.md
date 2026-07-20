# NetExplorer: Get Activity



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-signatures-by-signature-id-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-signatures-by-signature-id-activities?connectionId=$CONNECTION_ID&signatureId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-signatures-by-signature-id-activities?${params}`, {
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
| `signatureId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "date": "string",
      "from": 1,
      "id": 1,
      "signatureId": 1,
      "to": 1,
      "toUser": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string | Type d activité. |
| `date` | string | Date de l activité. |
| `from` | number | Identifiant source. |
| `id` | number | Identifiant de l activité. |
| `signatureId` | number | Identifiant de la signature. |
| `to` | number | Identifiant destination. |
| `toUser` | string | Utilisateur ciblé. |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /signatures/:signatureId/activities` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signatures-by-signature-id-activities.md) for the provider-specific parameters and requirements.

