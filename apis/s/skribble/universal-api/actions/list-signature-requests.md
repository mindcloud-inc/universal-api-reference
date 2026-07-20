# Skribble: List Signature Requests

Retrieves signature requests from Skribble.

```
GET https://connect.mindcloud.co/v1/universal/skribble/latest/actions/list-signature-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/list-signature-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribble/latest/actions/list-signature-requests?${params}`, {
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
| `accountEmail` | string | no | Filter by signer account email. |
| `pageNumber` | number | no | Page number starting at 0. |
| `pageSize` | number | no | Maximum results per page. |
| `search` | string | no | Search document titles containing this text. |
| `signatureStatus` | string | no | Filter by signer status code. |
| `statusOverall` | string | no | Filter by overall signature request status. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Skribble API returns.

## Native endpoint

Through the native Skribble API, this operation is `GET /v2/signature-requests` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signature-requests.md) for the provider-specific parameters and requirements.

