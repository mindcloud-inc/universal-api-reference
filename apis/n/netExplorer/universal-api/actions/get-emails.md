# NetExplorer: List Emails



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-emails?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "from": "string",
      "id": 1,
      "lastSend": "2026-05-07T12:00:00.000Z",
      "object": "string",
      "owner": "string",
      "ownerId": "string",
      "to": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Contenu de l email. |
| `from` | string | Adresse email de l expéditeur. |
| `id` | number | Identifiant numérique unique de l email. |
| `lastSend` | date | Date du dernier envoi. |
| `object` | string | Objet de l email. |
| `owner` | string | Nom complet du propriétaire de l email. |
| `ownerId` | string | Identifiant du propriétaire. |
| `to` | string | Destinataires séparés par des virgules. |
| `type` | string | Type de l email. |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /emails` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-emails.md) for the provider-specific parameters and requirements.

