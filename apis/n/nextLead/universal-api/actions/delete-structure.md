# NextLead: Delete Structure

Deletes an existing structure from NextLead.

```
DELETE https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/delete-structure
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/delete-structure?connectionId=$CONNECTION_ID&siret=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siret": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/delete-structure?${params}`, {
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
| `siret` | string | yes | Structure SIRET used to delete the structure. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "structure": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `structure` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native NextLead API, this operation is `POST /api/v2/receive/structure/delete-structure` (base URL `https://dashboard.nextlead.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-structure.md) for the provider-specific parameters and requirements.

