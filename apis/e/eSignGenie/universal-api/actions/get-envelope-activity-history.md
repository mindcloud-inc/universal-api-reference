# eSign Genie: Get Envelope Activity History

Retrieves envelope activity history from eSign Genie.

```
GET https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-envelope-activity-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-envelope-activity-history?connectionId=$CONNECTION_ID&folderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-envelope-activity-history?${params}`, {
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
| `folderId` | number | yes | The Foxit eSign envelope ID whose activity history should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {
        "activities": [
          {
            "action": "string",
            "activity": "string",
            "time": "string",
            "user": "string"
          }
        ],
        "folderId": 1,
        "latestActivityDate": "string",
        "status": "string"
      },
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details.activities[].action` | string |  |
| `details.activities[].activity` | string |  |
| `details.activities[].time` | string |  |
| `details.activities[].user` | string |  |
| `details.folderId` | number |  |
| `details.latestActivityDate` | string |  |
| `details.status` | string |  |
| `result` | string |  |

## Native endpoint

Through the native eSign Genie API, this operation is `GET /folders/viewActivityHistory` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-envelope-activity-history.md) for the provider-specific parameters and requirements.

