# Iris Dfir: Delete Note



```
DELETE https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/delete-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Iris Dfir `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/delete-note?connectionId=$CONNECTION_ID&identifier=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/delete-note?${params}`, {
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
| `identifier` | number | yes | IRIS note identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Iris Dfir API, this operation is `POST /case/notes/delete/:identifier` (base URL `https://v200.beta.dfir-iris.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-note.md) for the provider-specific parameters and requirements.

