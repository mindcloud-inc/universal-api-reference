# Hireflix: Get Position Interview Stats

Retrieves interview stats for a position in Hireflix.

```
GET https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-position-interview-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-position-interview-stats?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-position-interview-stats?${params}`, {
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
| `variables.id` | string | yes | The Hireflix position ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "total": 1,
      "totalArchived": 1,
      "totalCompleted": 1,
      "totalFinalist": 1,
      "totalPending": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total` | number |  |
| `totalArchived` | number |  |
| `totalCompleted` | number |  |
| `totalFinalist` | number |  |
| `totalPending` | number |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-position-interview-stats.md) for the provider-specific parameters and requirements.

