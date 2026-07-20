# Mifiel: Delete Stakeholder

Deletes a stakeholder from a document in Mifiel.

```
DELETE https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/delete-stakeholder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mifiel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/delete-stakeholder?connectionId=$CONNECTION_ID&documentId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/delete-stakeholder?${params}`, {
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
| `documentId` | string | yes | Document ID. |
| `id` | string | yes | Stakeholder ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mifiel API returns.

## Native endpoint

Through the native Mifiel API, this operation is `DELETE /api/v1/documents/:documentId/stakeholders/:id` (base URL `https://app.mifiel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-stakeholder.md) for the provider-specific parameters and requirements.

