# ActiveCampaign: Remove Tag From Contact

Removes a tag from a contact in ActiveCampaign.

```
DELETE https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/remove-tag-from-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCampaign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/remove-tag-from-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/remove-tag-from-contact?${params}`, {
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
| `id` | number | yes | The contact tag ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveCampaign API returns.

## Native endpoint

Through the native ActiveCampaign API, this operation is `DELETE /contactTags/:id` (base URL `{{credentials.apiUrl}}/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tag-from-contact.md) for the provider-specific parameters and requirements.

