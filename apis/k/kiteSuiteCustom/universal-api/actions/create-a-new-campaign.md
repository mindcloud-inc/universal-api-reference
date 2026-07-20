# Kite Suite: Create a new campaign



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-a-new-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-a-new-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-a-new-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `name` | string | yes | Name of the campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdBy": "string",
      "name": "Ava Chen",
      "schedules": [
        "string"
      ],
      "sequences": [
        "string"
      ],
      "status": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Campaign ID. |
| `createdBy` | string | Tenant ID. |
| `name` | string | Campaign name. |
| `schedules` | array<string> |  |
| `sequences` | array<string> |  |
| `status` | string | Campaign status. |
| `workspace` | string | Workspace ID. |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/campaign` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-new-campaign.md) for the provider-specific parameters and requirements.

