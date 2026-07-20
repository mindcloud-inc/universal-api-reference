# Encircle: Update Claim Note

Updates a claim note in Encircle.

```
PUT https://connect.mindcloud.co/v1/universal/encircle/latest/actions/update-claim-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encircle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/encircle/latest/actions/update-claim-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyClaimId": 1,
  "noteId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encircle/latest/actions/update-claim-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyClaimId": 1,
    "noteId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertyClaimId` | number | yes |  |
| `noteId` | number | yes |  |
| `title` | string | no |  |
| `text` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Encircle API returns.

## Native endpoint

Through the native Encircle API, this operation is `PATCH /v1/property_claims/:property_claim_id/notes/:note_id` (base URL `https://api.encircleapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-claim-note.md) for the provider-specific parameters and requirements.

