# Favro: Get Collection

Retrieves a collection from Favro by collection ID.

```
GET https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Favro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-collection?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-collection?${params}`, {
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
| `collectionId` | string | yes | The Favro collection ID to retrieve. |

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

Through the native Favro API, this operation is `GET /collections/:collectionId` (base URL `https://favro.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection.md) for the provider-specific parameters and requirements.

