# Wiza: Create List

Creates a Wiza list of people to enrich.

```
POST https://connect.mindcloud.co/v1/universal/wiza/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wiza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wiza/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wiza/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list` | object | yes | List configuration object including items and enrichment settings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "enrichment_level": "string",
        "finished_at": "string",
        "id": 1,
        "name": "Ava Chen",
        "stats": {
          "people": 1
        },
        "status": "string"
      },
      "status": {
        "code": 1,
        "message": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.enrichment_level` | string | Requested enrichment level. |
| `data.finished_at` | string | Completion timestamp when available. |
| `data.id` | number | List ID. |
| `data.name` | string | List name. |
| `data.stats.people` | number | Number of people in the list. |
| `data.status` | string | Current list status. |
| `status.code` | number | HTTP-style status code returned by Wiza. |
| `status.message` | string | Status message from Wiza. |
| `type` | string | Response type identifier. |

## Native endpoint

Through the native Wiza API, this operation is `POST /lists` (base URL `https://wiza.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

