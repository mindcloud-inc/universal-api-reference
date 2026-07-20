# Amberscript: Delete Glossary

Deletes an existing glossary from Amberscript.

```
DELETE https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/delete-glossary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amberscript `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/delete-glossary?connectionId=$CONNECTION_ID&glossaryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "glossaryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/delete-glossary?${params}`, {
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
| `glossaryId` | string | yes | Glossary to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amberscript API returns.

## Native endpoint

Through the native Amberscript API, this operation is `DELETE /glossary/:glossaryId` (base URL `https://api.amberscript.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-glossary.md) for the provider-specific parameters and requirements.

