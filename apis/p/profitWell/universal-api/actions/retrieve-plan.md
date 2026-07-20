# ProfitWell: Retrieve Plan

Retrieves a plan from ProfitWell.

```
GET https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/retrieve-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/retrieve-plan?connectionId=$CONNECTION_ID&id=foo_plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "foo_plan"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/retrieve-plan?${params}`, {
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
| `id` | string | yes | The ID of the manually-added plan you wish to retrieve or update. Example: `foo_plan`. |

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
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native ProfitWell API, this operation is `GET /v2/plans/:id/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-plan.md) for the provider-specific parameters and requirements.

