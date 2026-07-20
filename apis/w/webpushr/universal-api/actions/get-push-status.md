# Webpushr: Get Push Status



```
GET https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/get-push-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webpushr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/get-push-status?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/get-push-status?${params}`, {
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
| `campaignId` | string | yes | The push campaign ID returned when a notification campaign is created. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "campaignStatus": "string",
      "description": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string | The campaign identifier. |
| `campaignStatus` | string | The current delivery status for the campaign. |
| `description` | string | Additional status detail from Webpushr. |

## Native endpoint

Through the native Webpushr API, this operation is `GET /notification/status/id/:campaignId` (base URL `https://api.webpushr.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-push-status.md) for the provider-specific parameters and requirements.

