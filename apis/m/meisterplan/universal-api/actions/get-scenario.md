# Meisterplan: Get Scenario

Retrieves a scenario from Meisterplan.

```
GET https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-scenario
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-scenario?connectionId=$CONNECTION_ID&scenarioId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scenarioId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/get-scenario?${params}`, {
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
| `scenarioId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Scenario ID |
| `name` | string | Scenario name |

## Native endpoint

Through the native Meisterplan API, this operation is `GET /scenarios/:scenarioId` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scenario.md) for the provider-specific parameters and requirements.

