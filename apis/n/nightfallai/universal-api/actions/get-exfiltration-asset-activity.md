# Nightfall.ai: Get Exfiltration Asset Activity

Retrieves activity for an exfiltration asset from Nightfall.ai.

```
GET https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/get-exfiltration-asset-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nightfall.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/get-exfiltration-asset-activity?connectionId=$CONNECTION_ID&assetID=string&rangeStart=1&rangeEnd=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetID": "string",
  "rangeStart": "1",
  "rangeEnd": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/get-exfiltration-asset-activity?${params}`, {
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
| `assetID` | string | yes | The asset UUID whose exfiltration activity you want to fetch. |
| `rangeStart` | number | yes | Required Unix timestamp in seconds for the start of the activity window. |
| `rangeEnd` | number | yes | Required Unix timestamp in seconds for the end of the activity window. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activities": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities` | array<object> | Activity entries for the requested exfiltration asset and time window. |

## Native endpoint

Through the native Nightfall.ai API, this operation is `GET /exfiltration/v1/asset/activity` (base URL `https://api.nightfall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-exfiltration-asset-activity.md) for the provider-specific parameters and requirements.

