# Doppler Marketing Automation: Get List

Retrieves a list from Doppler Marketing Automation.

```
GET https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Marketing Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/get-list?connectionId=$CONNECTION_ID&listId=509702" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "509702"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/get-list?${params}`, {
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
| `listId` | string | yes | Doppler list identifier. Example: `509702`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": [
        {}
      ],
      "creationDate": "2026-05-07T12:00:00.000Z",
      "currentStatus": "string",
      "listId": 1,
      "name": "Ava Chen",
      "subscribersCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | array<object> |  |
| `creationDate` | date |  |
| `currentStatus` | string |  |
| `listId` | number |  |
| `name` | string |  |
| `subscribersCount` | number |  |

## Native endpoint

Through the native Doppler Marketing Automation API, this operation is `GET /accounts/:accountName/lists/:listId` (base URL `https://restapi.fromdoppler.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

