# Algolia: Retrieve a Synonym

Retrieves an existing synonym from Algolia.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-a-synonym
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-a-synonym?connectionId=$CONNECTION_ID&indexName=Ava%20Chen&objectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indexName": "Ava Chen",
  "objectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-a-synonym?${params}`, {
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
| `indexName` | string | yes | Name of the index on which to retrieve the synonym. |
| `objectId` | string | yes | Unique identifier of the synonym object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "objectID": "string",
      "synonyms": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `objectID` | string |  |
| `synonyms` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native Algolia API, this operation is `GET /1/indexes/:indexName/synonyms/:objectID` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-a-synonym.md) for the provider-specific parameters and requirements.

