# Campaign Monitor: Get List Details

Retrieves details for a Campaign Monitor list.

```
GET https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-list-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-list-details?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/get-list-details?${params}`, {
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
| `listId` | string | yes | Campaign Monitor list identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confirmationSuccessPage": "string",
      "confirmedOptIn": true,
      "listId": "string",
      "title": "string",
      "unsubscribePage": "string",
      "unsubscribeSetting": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmationSuccessPage` | string | URL used after confirmation succeeds. |
| `confirmedOptIn` | boolean | Whether the list requires confirmed opt-in. |
| `listId` | string | Campaign Monitor list identifier. |
| `title` | string | Campaign Monitor list title. |
| `unsubscribePage` | string | URL for the list unsubscribe page. |
| `unsubscribeSetting` | string | Campaign Monitor unsubscribe behavior for the list. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `GET /lists/:listId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-details.md) for the provider-specific parameters and requirements.

