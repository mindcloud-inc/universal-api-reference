# Incontrol: Get Organization

Retrieves details for an organization from Incontrol.

```
GET https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Incontrol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-organization?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/get-organization?${params}`, {
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
| `id` | string | yes | The organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "expiredDate": "2026-05-07T12:00:00.000Z",
      "groups": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "paymentPlan": "string",
      "rights": [
        "string"
      ],
      "updated": "2026-05-07T12:00:00.000Z",
      "userSlots": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Creation timestamp. |
| `expiredDate` | date | Plan expiration timestamp. |
| `groups` | array<object> | Groups associated with the organization. |
| `id` | string | Organization ID. |
| `name` | string | Organization name. |
| `paymentPlan` | string | Payment plan name. |
| `rights` | array<string> | Organization rights available to the token. |
| `updated` | date | Last update timestamp. |
| `userSlots` | number | Number of user slots included in the plan. |

## Native endpoint

Through the native Incontrol API, this operation is `GET /api/v1/organization/{{id}}` (base URL `https://portal.incontrol.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

