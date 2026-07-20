# Virtually: List Automations

Retrieves automations from your Virtually workspace.

```
GET https://connect.mindcloud.co/v1/universal/virtually/latest/actions/list-automations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/list-automations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/virtually/latest/actions/list-automations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {}
      ],
      "automationId": "string",
      "createdAt": 1,
      "CreatedBy": {},
      "name": "Ava Chen",
      "orgId": "string",
      "Trigger": {},
      "triggerId": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<object> |  |
| `automationId` | string |  |
| `createdAt` | number |  |
| `CreatedBy` | object |  |
| `name` | string |  |
| `orgId` | string |  |
| `Trigger` | object |  |
| `triggerId` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Virtually API, this operation is `GET /api/v2/orgs/:orgId/automations` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-automations.md) for the provider-specific parameters and requirements.

