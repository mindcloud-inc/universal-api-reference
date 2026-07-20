# UpViral: List Custom Fields

Retrieves campaign custom fields from UpViral.

```
GET https://connect.mindcloud.co/v1/universal/upViral/latest/actions/list-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpViral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upViral/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID&campaign_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaign_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upViral/latest/actions/list-custom-fields?${params}`, {
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
| `campaign_id` | string | yes | The UpViral campaign ID whose custom fields should be listed. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UpViral API returns.

## Native endpoint

Through the native UpViral API, this operation is `POST /` (base URL `https://app.upviral.com/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-fields.md) for the provider-specific parameters and requirements.

