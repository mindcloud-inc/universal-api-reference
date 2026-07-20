# GoTeamup: Get Membership Allotment

Retrieves membership allotment details from GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/get-membership-allotment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/get-membership-allotment?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/get-membership-allotment?${params}`, {
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
| `id` | number | yes | The TeamUp membership ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ignoreNoShows": true,
      "periodLimits": [
        {
          "maxUses": 1,
          "period": "string",
          "type": "string"
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
| `ignoreNoShows` | boolean |  |
| `periodLimits[].maxUses` | number |  |
| `periodLimits[].period` | string |  |
| `periodLimits[].type` | string |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /memberships/:id/allotment` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-membership-allotment.md) for the provider-specific parameters and requirements.

