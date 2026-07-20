# Countly: List Campaigns

Retrieves all campaigns from Countly.

```
GET https://connect.mindcloud.co/v1/universal/countly/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Countly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/countly/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/countly/latest/actions/list-campaigns?${params}`, {
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
| `appId` | string | yes | Countly app ID to list campaigns for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaigns": [
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
| `campaigns` | array<object> | Campaign rows when the Countly campaign endpoint is available. |

## Native endpoint

Through the native Countly API, this operation is `GET /o/campaign` (base URL `https://mindcloud-fe49f15890040.flex.countly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

