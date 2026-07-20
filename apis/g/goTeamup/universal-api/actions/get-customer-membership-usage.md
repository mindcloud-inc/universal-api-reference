# GoTeamup: Get Customer Membership Usage

Retrieves customer membership usage from GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/get-customer-membership-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/get-customer-membership-usage?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/get-customer-membership-usage?${params}`, {
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
| `id` | number | yes | The TeamUp customer membership ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "usagePeriods": [
        {
          "endDate": {},
          "maxUses": 1,
          "periodType": "string",
          "prorateAdjustment": {},
          "remainingCount": 1,
          "startDate": {},
          "usedCount": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `usagePeriods[].endDate` | object |  |
| `usagePeriods[].maxUses` | number |  |
| `usagePeriods[].periodType` | string |  |
| `usagePeriods[].prorateAdjustment` | object |  |
| `usagePeriods[].remainingCount` | number |  |
| `usagePeriods[].startDate` | object |  |
| `usagePeriods[].usedCount` | number |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /customer_memberships/:id/usage` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-membership-usage.md) for the provider-specific parameters and requirements.

