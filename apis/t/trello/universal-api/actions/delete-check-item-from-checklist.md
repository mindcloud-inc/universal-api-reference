# Trello: Delete CheckItem from Checklist

Deletes a check item from a Trello checklist.

```
DELETE https://connect.mindcloud.co/v1/universal/trello/latest/actions/delete-check-item-from-checklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/trello/latest/actions/delete-check-item-from-checklist?connectionId=$CONNECTION_ID&id=string&idCheckItem=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "idCheckItem": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trello/latest/actions/delete-check-item-from-checklist?${params}`, {
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
| `id` | string | yes | Checklist identifier. |
| `idCheckItem` | string | yes | Checklist item identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limits": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limits` | object |  |

## Native endpoint

Through the native Trello API, this operation is `DELETE checklists/:id/checkItems/:idCheckItem` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-check-item-from-checklist.md) for the provider-specific parameters and requirements.

