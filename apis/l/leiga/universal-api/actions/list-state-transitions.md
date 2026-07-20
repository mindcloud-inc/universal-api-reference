# Leiga: List State Transitions

Retrieves available state transitions from Leiga.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-state-transitions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-state-transitions?connectionId=$CONNECTION_ID&defId=1&stateId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "defId": "1",
  "stateId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-state-transitions?${params}`, {
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
| `defId` | number | yes | Workflow ID |
| `stateId` | number | yes | State ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "stateCategory": 1,
      "stateId": 1,
      "stateName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stateCategory` | number |  |
| `stateId` | number |  |
| `stateName` | string |  |

## Native endpoint

Through the native Leiga API, this operation is `POST /workflow/list/next-state` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-state-transitions.md) for the provider-specific parameters and requirements.

