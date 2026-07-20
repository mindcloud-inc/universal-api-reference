# lemlist: List Campaign Sequences

Retrieves sequences from a lemlist campaign.

```
GET https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-campaign-sequences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-campaign-sequences?connectionId=$CONNECTION_ID&campaignId=67618ad126d28d06429eb1c4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "67618ad126d28d06429eb1c4"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/list-campaign-sequences?${params}`, {
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
| `campaignId` | string | yes | The ID of the campaign whose sequences should be retrieved. Example: `67618ad126d28d06429eb1c4`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native lemlist API returns.

## Native endpoint

Through the native lemlist API, this operation is `GET /campaigns/:campaignId/sequences` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-sequences.md) for the provider-specific parameters and requirements.

