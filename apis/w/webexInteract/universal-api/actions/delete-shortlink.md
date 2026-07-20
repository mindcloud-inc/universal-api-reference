# Webex Interact: Delete shortlink

Deletes an existing shortlink from Webex Interact.

```
DELETE https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/delete-shortlink
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/delete-shortlink?connectionId=$CONNECTION_ID&linkId=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkId": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/delete-shortlink?${params}`, {
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
| `linkId` | string | yes | Shortlink ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "linkId": "https://example.com",
      "status_code": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `linkId` | string |  |
| `status_code` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Webex Interact API, this operation is `DELETE /assets/v1/shortlink/{linkId}` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-shortlink.md) for the provider-specific parameters and requirements.

