# Favro: Get All Collections

Retrieves collections from Favro.

```
GET https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-all-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Favro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-all-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-all-collections?${params}`, {
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
| `archived` | boolean | no | Return archived collections when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "background": "string",
      "collectionId": "string",
      "fullMembersCanAddWidgets": true,
      "name": "Ava Chen",
      "organizationId": "string",
      "publicSharing": "string",
      "sharedToUsers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `background` | string |  |
| `collectionId` | string |  |
| `fullMembersCanAddWidgets` | boolean |  |
| `name` | string |  |
| `organizationId` | string |  |
| `publicSharing` | string |  |
| `sharedToUsers` | array<object> |  |

## Native endpoint

Through the native Favro API, this operation is `GET /collections` (base URL `https://favro.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-collections.md) for the provider-specific parameters and requirements.

