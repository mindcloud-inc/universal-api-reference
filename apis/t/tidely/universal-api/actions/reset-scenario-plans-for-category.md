# Tidely: Reset Scenario Plans For Category



```
DELETE https://connect.mindcloud.co/v1/universal/tidely/latest/actions/reset-scenario-plans-for-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tidely/latest/actions/reset-scenario-plans-for-category?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidely/latest/actions/reset-scenario-plans-for-category?${params}`, {
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
| `categoryId` | string | no | Tidely category ID whose scenario plans should be reset. |
| `scenarioId` | string | no | Tidely scenario ID whose plans should be reset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the delete operation succeeded. |

## Native endpoint

Through the native Tidely API, this operation is `DELETE /api/v1/open-api/plans` (base URL `https://api.tidely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reset-scenario-plans-for-category.md) for the provider-specific parameters and requirements.

