# YNAB: List Money Movement Groups

Retrieves money movement groups from a YNAB plan.

```
GET https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-money-movement-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YNAB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-money-movement-groups?connectionId=$CONNECTION_ID&planId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-money-movement-groups?${params}`, {
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
| `planId` | string | yes | The id of the plan. You can also use last-used or default when enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupCreatedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "month": "2026-05-07T12:00:00.000Z",
      "note": "string",
      "performedByUserId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupCreatedAt` | date | When the money movement group was created. |
| `id` | string | The money movement group ID. |
| `month` | date | The month of the money movement group. |
| `note` | string | The money movement group note, when present. |
| `performedByUserId` | string | The user who performed the money movement group, when present. |

## Native endpoint

Through the native YNAB API, this operation is `GET /plans/:planId/money_movement_groups` (base URL `https://api.ynab.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-money-movement-groups.md) for the provider-specific parameters and requirements.

