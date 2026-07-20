# Matomo: OAuth2 update Client



```
PUT https://connect.mindcloud.co/v1/universal/matomo/latest/actions/o-auth2-update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/o-auth2-update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "name": "Ava Chen",
  "grantTypes": "string",
  "scope": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/matomo/latest/actions/o-auth2-update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "name": "Ava Chen",
    "grantTypes": "string",
    "scope": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | Matomo API parameter. |
| `name` | string | yes | Matomo API parameter. |
| `grantTypes` | string | yes | Matomo API parameter. |
| `scope` | string | yes | Matomo API parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `redirectUris` | string | no | Matomo API parameter. Default: `Array`. |
| `description` | string | no | Matomo API parameter. |
| `type` | string | no | Matomo API parameter. Default: `confidential`. |
| `active` | string | no | Matomo API parameter. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string",
      "nb_actions": 1,
      "nb_visits": 1,
      "result": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string | Matomo response label |
| `nb_actions` | number | Actions |
| `nb_visits` | number | Visits |
| `result` | string | Operation result |
| `value` | string | Matomo response value |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/o-auth2-update-client.md) for the provider-specific parameters and requirements.

