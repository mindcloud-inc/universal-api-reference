# Sarbacane: Get Campaign Statistics

Retrieves campaign statistics from your Sarbacane account.

```
GET https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/get-campaign-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sarbacane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/get-campaign-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/get-campaign-statistics?${params}`, {
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
| `campaignId` | string | no | Sarbacane campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sendId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sendId` | object | Statistics payload keyed by send identifier. |

## Native endpoint

Through the native Sarbacane API, this operation is `GET /reports/{campaignId}` (base URL `https://api.sarbacane.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-statistics.md) for the provider-specific parameters and requirements.

