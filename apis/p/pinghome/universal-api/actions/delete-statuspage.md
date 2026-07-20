# Pinghome: Delete Statuspage

Deletes an existing statuspage from Pinghome.

```
DELETE https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/delete-statuspage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/delete-statuspage?connectionId=$CONNECTION_ID&statuspageId=74f926a6-8cfc-4f11-86e6-46e7193813a8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "statuspageId": "74f926a6-8cfc-4f11-86e6-46e7193813a8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/delete-statuspage?${params}`, {
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
| `statuspageId` | string | yes | Statuspage ID to delete. Example: `74f926a6-8cfc-4f11-86e6-46e7193813a8`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `DELETE /statuspage-cmd/v1/statuspage/:id` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-statuspage.md) for the provider-specific parameters and requirements.

