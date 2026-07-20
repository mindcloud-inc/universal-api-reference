# GrowthBook: Update a member's global role (including any enviroment restrictions, if applicable). Can also update a member's project roles if your plan supports it.

Updates a member role in GrowthBook.

```
PUT https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-member-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-member-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7",
  "member": {
    "sample": "value"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-member-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prj_19g6smo332up7",
    "member": {"sample":"value"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The id of the requested resource Default: `prj_19g6smo332up7`. |
| `member` | object | yes | Default: `{"sample":"value"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updatedMember": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updatedMember` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /members/:id/role` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-member-role.md) for the provider-specific parameters and requirements.

