# Countly: Get Campaign Data

Retrieves all campaign data from Countly.

```
GET https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-campaign-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Countly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-campaign-data?connectionId=$CONNECTION_ID&appId=string&data=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "data": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-campaign-data?${params}`, {
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
| `appId` | string | yes | Countly app ID to query campaign data for. |
| `data` | string | yes | JSON string array of campaign IDs to fetch action data for. |
| `period` | string | no | Countly reporting period, such as month, 60days, 30days, 7days, yesterday, or today. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Campaign analytics data for the requested campaign IDs. |

## Native endpoint

Through the native Countly API, this operation is `GET /o/campaign` (base URL `https://mindcloud-fe49f15890040.flex.countly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-data.md) for the provider-specific parameters and requirements.

