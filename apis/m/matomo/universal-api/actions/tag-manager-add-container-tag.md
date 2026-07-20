# Matomo: TagManager add Container Tag



```
POST https://connect.mindcloud.co/v1/universal/matomo/latest/actions/tag-manager-add-container-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/tag-manager-add-container-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idSite": "1",
  "idContainer": "string",
  "idContainerVersion": "string",
  "type": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/matomo/latest/actions/tag-manager-add-container-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idSite": "1",
    "idContainer": "string",
    "idContainerVersion": "string",
    "type": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idSite` | number | yes | Matomo API parameter. Default: `1`. |
| `idContainer` | string | yes | Matomo API parameter. |
| `idContainerVersion` | string | yes | Matomo API parameter. |
| `type` | string | yes | Matomo API parameter. |
| `name` | string | yes | Matomo API parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parameters` | string | no | Matomo API parameter. Default: `Array`. |
| `fireTriggerIds` | string | no | Matomo API parameter. Default: `Array`. |
| `blockTriggerIds` | string | no | Matomo API parameter. Default: `Array`. |
| `fireLimit` | string | no | Matomo API parameter. Default: `unlimited`. |
| `fireDelay` | string | no | Matomo API parameter. Default: `0`. |
| `priority` | string | no | Matomo API parameter. Default: `999`. |
| `startDate` | string | no | Matomo API parameter. |
| `endDate` | string | no | Matomo API parameter. |
| `description` | string | no | Matomo API parameter. |
| `status` | string | no | Matomo API parameter. |

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

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tag-manager-add-container-tag.md) for the provider-specific parameters and requirements.

