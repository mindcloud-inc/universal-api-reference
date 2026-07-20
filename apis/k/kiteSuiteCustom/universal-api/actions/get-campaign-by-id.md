# Kite Suite: Get campaign by ID



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-campaign-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-campaign-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-campaign-by-id?${params}`, {
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
| `id` | string | yes | Campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "campaignStart": "string",
      "createdAt": "string",
      "createdBy": "string",
      "end": "string",
      "isTrashed": true,
      "leads": [
        "string"
      ],
      "name": "Ava Chen",
      "options": {},
      "schedules": [
        "string"
      ],
      "sequences": [
        "string"
      ],
      "start": "string",
      "status": "string",
      "unsubscribe": [
        "string"
      ],
      "updatedAt": "string",
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
| `campaignStart` | string | Campaign start time. |
| `createdAt` | string | Campaign creation timestamp. |
| `createdBy` | string | User ID of the campaign creator. |
| `end` | string | End date of the campaign. |
| `isTrashed` | boolean | Flag indicating if the campaign is trashed. |
| `leads` | array<string> |  |
| `name` | string | Name of the campaign. |
| `options` | object |  |
| `schedules` | array<string> |  |
| `sequences` | array<string> |  |
| `start` | string | Start date of the campaign. |
| `status` | string | Campaign status. |
| `unsubscribe` | array |  |
| `updatedAt` | string | Campaign last update timestamp. |
| `workspace` | string | Workspace ID associated with the campaign. |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/campaign/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-by-id.md) for the provider-specific parameters and requirements.

