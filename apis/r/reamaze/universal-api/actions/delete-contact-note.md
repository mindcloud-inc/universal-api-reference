# Reamaze: Delete Contact Note



```
DELETE https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/delete-contact-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/delete-contact-note?connectionId=$CONNECTION_ID&contactIdentifier=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactIdentifier": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/delete-contact-note?${params}`, {
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
| `contactIdentifier` | string | yes | Path parameter for email\|phone. |
| `id` | string | yes | Path parameter for id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Reamaze API returns.

## Native endpoint

Through the native Reamaze API, this operation is `DELETE /contacts/:contactIdentifier/notes/:id` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-note.md) for the provider-specific parameters and requirements.

