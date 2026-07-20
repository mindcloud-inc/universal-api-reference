# Dotdigital: Get Campaign Send Status

Retrieves a campaign send status from Dotdigital by send ID.

```
GET https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-campaign-send-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotdigital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-campaign-send-status?connectionId=$CONNECTION_ID&id=842d81e8-c619-457f-bb77-ab6c4a17da39" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "842d81e8-c619-457f-bb77-ab6c4a17da39"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-campaign-send-status?${params}`, {
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
| `id` | string | yes | The GUID returned by the send campaign call. Example: `842d81e8-c619-457f-bb77-ab6c4a17da39`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dotdigital API returns.

## Native endpoint

Through the native Dotdigital API, this operation is `GET /v2/campaigns/send/:id` (base URL `https://r2-api.dotmailer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-send-status.md) for the provider-specific parameters and requirements.

