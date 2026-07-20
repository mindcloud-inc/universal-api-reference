# Matomo: TagManager get Available Tag Types In Context



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/tag-manager-get-available-tag-types-in-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/tag-manager-get-available-tag-types-in-context?connectionId=$CONNECTION_ID&idContext=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idContext": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/tag-manager-get-available-tag-types-in-context?${params}`, {
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
| `idContext` | string | yes | Matomo API parameter. |

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

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tag-manager-get-available-tag-types-in-context.md) for the provider-specific parameters and requirements.

