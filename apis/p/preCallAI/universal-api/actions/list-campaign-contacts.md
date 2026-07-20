# PreCallAI: List Campaign Contacts

Retrieves campaign contacts from PreCallAI.

```
GET https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-campaign-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PreCallAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-campaign-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-campaign-contacts?${params}`, {
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
| `id` | string | no | The campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "message": "string",
      "statistics": {
        "totalCallAnswered": 1,
        "totalCallFailed": 1,
        "totalCallPlaced": 1,
        "totalVoiceConsumed": 1
      },
      "status": 1,
      "success": true,
      "totalItems": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of campaign contacts returned by PreCallAI. |
| `message` | string | Provider status message for campaign contacts. |
| `statistics` | object | Aggregate campaign contact statistics returned by PreCallAI. |
| `statistics.totalCallAnswered` | number | Total calls answered. |
| `statistics.totalCallFailed` | number | Total calls failed. |
| `statistics.totalCallPlaced` | number | Total calls placed. |
| `statistics.totalVoiceConsumed` | number | Total voice consumed. |
| `status` | number | HTTP-style status returned by PreCallAI. |
| `success` | boolean | Whether the campaign contacts request succeeded. |
| `totalItems` | number | Total items available in the campaign contacts result. |
| `totalPages` | number | Total pages available in the campaign contacts result. |

## Native endpoint

Through the native PreCallAI API, this operation is `POST /campaign/audiences` (base URL `https://api.precallai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-contacts.md) for the provider-specific parameters and requirements.

