# EmailOctopus: Get Campaign Report: Unsubscribed

Retrieves the unsubscribed report for an EmailOctopus campaign.

```
GET https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/get-campaign-report-unsubscribed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailOctopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/get-campaign-report-unsubscribed?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailOctopus/latest/actions/get-campaign-report-unsubscribed?${params}`, {
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
| `campaignId` | string | yes | The unique ID of the campaign. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EmailOctopus API returns.

## Native endpoint

Through the native EmailOctopus API, this operation is `GET /campaigns/:campaignId/report/unsubscribed` (base URL `https://emailoctopus.com/api/1.6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-report-unsubscribed.md) for the provider-specific parameters and requirements.

