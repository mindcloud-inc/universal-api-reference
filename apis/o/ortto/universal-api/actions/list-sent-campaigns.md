# Ortto: List Sent Campaigns



```
GET https://connect.mindcloud.co/v1/universal/ortto/latest/actions/list-sent-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/list-sent-campaigns?connectionId=$CONNECTION_ID&start=%5Bobject%20Object%5D&end=%5Bobject%20Object%5D&timezone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "[object Object]",
  "end": "[object Object]",
  "timezone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ortto/latest/actions/list-sent-campaigns?${params}`, {
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
| `start` | object | yes | Calendar window start with year and month keys. |
| `end` | object | yes | Calendar window end with year and month keys. |
| `timezone` | string | yes | IANA timezone used for the calendar window. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "totalActiveCampaigns": 1,
        "totalCampaigns": 1
      },
      "today": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.totalActiveCampaigns` | number |  |
| `meta.totalCampaigns` | number |  |
| `today` | string |  |

## Native endpoint

Through the native Ortto API, this operation is `POST /campaign/calendar` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sent-campaigns.md) for the provider-specific parameters and requirements.

