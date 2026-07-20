# SigningHub: Recall Document

Recalls a document workflow in SigningHub.

```
DELETE https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/recall-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/recall-document?connectionId=$CONNECTION_ID&packageId=11191542" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageId": "11191542"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/recall-document?${params}`, {
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
| `packageId` | number | yes | The shared document package to recall. Example: `11191542`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SigningHub API returns.

## Native endpoint

Through the native SigningHub API, this operation is `DELETE /v4/packages/:packageId/workflow` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/recall-document.md) for the provider-specific parameters and requirements.

