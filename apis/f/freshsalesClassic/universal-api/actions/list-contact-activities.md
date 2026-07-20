# Freshsales Classic: List Contact Activities

Retrieves activities for a contact from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-contact-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-contact-activities?connectionId=$CONNECTION_ID&id=127081207857" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "127081207857"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-contact-activities?${params}`, {
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
| `id` | number | yes | Freshsales contact id to inspect for timeline activities. Example: `127081207857`. |
| `include` | string | no | Optional embedded resources, such as user. Example: `user`. |
| `limit` | number | no | Maximum number of activities to return. Default: `10`. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionableId": 1,
      "actionableType": "string",
      "actionData": {},
      "actionType": "string",
      "additionalTimelineInfo": {},
      "compositeId": "string",
      "createdAt": "string",
      "id": "string",
      "targetableId": 1,
      "targetableType": "string",
      "userActivity": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionableId` | number |  |
| `actionableType` | string |  |
| `actionData` | object |  |
| `actionType` | string |  |
| `additionalTimelineInfo` | object |  |
| `compositeId` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `targetableId` | number |  |
| `targetableType` | string |  |
| `userActivity` | boolean |  |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /contacts/:id/activities` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-activities.md) for the provider-specific parameters and requirements.

