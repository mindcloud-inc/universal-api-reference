# UpViral: Get Contact

Retrieves a campaign contact from UpViral.

```
GET https://connect.mindcloud.co/v1/universal/upViral/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpViral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upViral/latest/actions/get-contact?connectionId=$CONNECTION_ID&campaign_id=string&lead_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaign_id": "string",
  "lead_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upViral/latest/actions/get-contact?${params}`, {
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
| `campaign_id` | string | yes | The UpViral campaign ID containing the contact. |
| `lead_id` | string | yes | The contact's UpViral lead ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UpViral API returns.

## Native endpoint

Through the native UpViral API, this operation is `POST /` (base URL `https://app.upviral.com/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

