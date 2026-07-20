# Timeular: V2 Archive an Activity

Deletes an activity from the Timeular v2 API.

```
DELETE https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-archive-an-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-archive-an-activity?connectionId=$CONNECTION_ID&activityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-archive-an-activity?${params}`, {
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
| `activityId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors[]` | array<string> |  |

## Native endpoint

Through the native Timeular API, this operation is `DELETE /api/v2/activities/:activityId` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-archive-an-activity.md) for the provider-specific parameters and requirements.

