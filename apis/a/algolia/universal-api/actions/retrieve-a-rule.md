# Algolia: Retrieve a Rule

Retrieves an existing rule from Algolia.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-a-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-a-rule?connectionId=$CONNECTION_ID&indexName=Ava%20Chen&objectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indexName": "Ava Chen",
  "objectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-a-rule?${params}`, {
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
| `indexName` | string | yes | Name of the index on which to retrieve the rule. |
| `objectId` | string | yes | Unique identifier of the rule object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conditions": [
        {}
      ],
      "consequence": {},
      "description": "string",
      "enabled": true,
      "objectID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conditions` | array<object> |  |
| `consequence` | object |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `objectID` | string |  |

## Native endpoint

Through the native Algolia API, this operation is `GET /1/indexes/:indexName/rules/:objectID` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-a-rule.md) for the provider-specific parameters and requirements.

