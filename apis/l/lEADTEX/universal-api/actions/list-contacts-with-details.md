# LEADTEX: List Contacts With Details

Retrieves contacts with related details from LEADTEX.

```
GET https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-contacts-with-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-contacts-with-details?connectionId=$CONNECTION_ID&with=tags%2Cvariables" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "with": "tags,variables"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/list-contacts-with-details?${params}`, {
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
| `with` | string | yes | Additional contact entities to include. Use tags,variables for this action. Default: `tags,variables`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "bot_id": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "id": 1,
        "messenger": "string",
        "name": "Ava Chen",
        "phone": "string",
        "tags": [
          "string"
        ],
        "variables": [
          {}
        ]
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
| `data.bot_id` | number |  |
| `data.created_at` | date |  |
| `data.email` | string |  |
| `data.id` | number |  |
| `data.messenger` | string |  |
| `data.name` | string |  |
| `data.phone` | string |  |
| `data.tags` | array<string> |  |
| `data.variables` | array<object> |  |
| `links` | object |  |
| `meta` | object |  |

## Native endpoint

Through the native LEADTEX API, this operation is `GET /getContacts?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts-with-details.md) for the provider-specific parameters and requirements.

