# Campaign Refinery: Get Contact Tags

Retrieves tags for a contact from Campaign Refinery.

```
GET https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-contact-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Refinery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-contact-tags?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-contact-tags?${params}`, {
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
| `id` | string | yes | Campaign Refinery contact ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Campaign Refinery API returns.

## Native endpoint

Through the native Campaign Refinery API, this operation is `GET /contacts/get-contact-tags` (base URL `https://app.campaignrefinery.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-tags.md) for the provider-specific parameters and requirements.

