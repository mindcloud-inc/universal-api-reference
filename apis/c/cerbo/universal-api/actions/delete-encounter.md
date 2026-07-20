# Cerbo: Delete Encounter

Deletes an existing encounter from Cerbo.

```
DELETE https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/delete-encounter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/delete-encounter?connectionId=$CONNECTION_ID&encounter_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "encounter_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/delete-encounter?${params}`, {
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
| `encounter_id` | number | yes | Encounter identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "data": "string",
      "id": 1,
      "message": "string",
      "object": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `data` | string |  |
| `id` | number |  |
| `message` | string |  |
| `object` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Cerbo API, this operation is `DELETE /encounters/:encounter_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-encounter.md) for the provider-specific parameters and requirements.

