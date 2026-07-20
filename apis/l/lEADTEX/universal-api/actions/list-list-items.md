# LEADTEX: List List Items

Retrieves list items from a LEADTEX list.

```
GET https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-list-items?connectionId=$CONNECTION_ID&schema_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schema_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-list-items?${params}`, {
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
| `schema_id` | string | yes | ID of the list schema whose items should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contact_id": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "links": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data.contact_id` | number |  |
| `data.created_at` | date |  |
| `data.id` | string |  |
| `data.updated_at` | date |  |
| `links` | object |  |
| `meta` | object |  |

## Native endpoint

Through the native LEADTEX API, this operation is `POST /getListItems?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-list-items.md) for the provider-specific parameters and requirements.

