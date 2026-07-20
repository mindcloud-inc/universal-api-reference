# snapADDY: List Questionnaires



```
GET https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/list-questionnaires
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a snapADDY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/list-questionnaires?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/list-questionnaires?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of questionnaires to return |
| `page` | number | no | Page number |
| `finalizedOnly` | boolean | no | Filter for finalized questionnaires only |
| `order` | string | no | Sort order expression |
| `filter` | string | no | Filter expression |
| `search` | string | no | Search term |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "contactListId": "string",
      "created": "string",
      "defaultLanguage": "string",
      "finalized": true,
      "id": "string",
      "languages": [
        "string"
      ],
      "organizationId": "string",
      "titles": {},
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `contactListId` | string |  |
| `created` | string |  |
| `defaultLanguage` | string |  |
| `finalized` | boolean |  |
| `id` | string |  |
| `languages` | array<string> |  |
| `organizationId` | string |  |
| `titles` | object |  |
| `updated` | string |  |

## Native endpoint

Through the native snapADDY API, this operation is `GET /visitreport/v1/backend/questionnaires/all` (base URL `https://api.snapaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-questionnaires.md) for the provider-specific parameters and requirements.

