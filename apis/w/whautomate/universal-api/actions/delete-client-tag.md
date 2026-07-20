# Whautomate: Delete Client Tag

Deletes an existing client tag from Whautomate.

```
DELETE https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/delete-client-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whautomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/delete-client-tag?connectionId=$CONNECTION_ID&clientTagId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientTagId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/delete-client-tag?${params}`, {
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
| `clientTagId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Whautomate API, this operation is `DELETE /v1/clientTags/{{clientTagId}}` (base URL `https://api.whautomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-client-tag.md) for the provider-specific parameters and requirements.

