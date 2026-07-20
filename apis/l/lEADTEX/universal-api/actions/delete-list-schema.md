# LEADTEX: Delete List Schema

Deletes a list schema from LEADTEX.

```
DELETE https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/delete-list-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/delete-list-schema?connectionId=$CONNECTION_ID&schema_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schema_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/delete-list-schema?${params}`, {
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
| `schema_id` | string | yes | ID of the list schema to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "errors": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `errors` | object |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native LEADTEX API, this operation is `POST /deleteListSchema?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-list-schema.md) for the provider-specific parameters and requirements.

