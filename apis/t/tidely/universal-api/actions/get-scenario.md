# Tidely: Get Scenario



```
GET https://connect.mindcloud.co/v1/universal/tidely/latest/actions/get-scenario
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidely/latest/actions/get-scenario?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidely/latest/actions/get-scenario?${params}`, {
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
| `scenarioId` | string | no | Tidely scenario ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "isBaseCase": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Tidely scenario ID. |
| `isBaseCase` | boolean | Whether the scenario is the base case. |
| `name` | string | Scenario name. |

## Native endpoint

Through the native Tidely API, this operation is `GET /api/v1/open-api/scenarios/:scenarioId` (base URL `https://api.tidely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scenario.md) for the provider-specific parameters and requirements.

