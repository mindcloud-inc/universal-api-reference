# NetExplorer: Update Invite



```
PUT https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-invite-by-invitation-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-invite-by-invitation-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invitationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/update-invite-by-invitation-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invitationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invitationId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiration": "2026-05-07T12:00:00.000Z",
      "folder": 1,
      "id": "string",
      "key": "string",
      "rights": 1,
      "source": "string",
      "sourceName": "Ava Chen",
      "target": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiration` | date | Date d'expiration de l'invitation. Arrivé à échéance, l'utilisateur invité ne pourra pas créer de compte avec cette invitation. |
| `folder` | number | Identifiant du dossier auquel l'utilisateur aura accès une fois son compte crée. |
| `id` | string | Identifiant unique de l'invitation. |
| `key` | string | Clé de l'invitation qui va permettre à l'utilisateur de procéder à la modification de son compte. |
| `rights` | number | Correspondance des droits à appliquer à la création du compte. ValeurDroits 1Lecture |
| `source` | string | Identifiant de l'utilisateur ayant procédé à l'invitation. |
| `sourceName` | string | Nom de l'utilisateur ayant procédé à l'invitation. |
| `target` | number | Identifiant de l'utilisateur crée suite à l'invitation. |

## Native endpoint

Through the native NetExplorer API, this operation is `PUT /invite/:invitationId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invite-by-invitation-id.md) for the provider-specific parameters and requirements.

