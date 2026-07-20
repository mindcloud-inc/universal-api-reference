# InsightIQ: List Professional Topics

Finds professional topics in InsightIQ by keyword.

```
GET https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/list-professional-topics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InsightIQ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/list-professional-topics?connectionId=$CONNECTION_ID&limit=25&offset=0&identifier=string&workPlatformId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "identifier": "string",
  "workPlatformId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/list-professional-topics?${params}`, {
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
| `identifier` | string | yes | Topic keyword or prefix to search. |
| `workPlatformId` | string | yes | InsightIQ work platform identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "topics": [
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
| `metadata` | object |  |
| `topics` | array<object> |  |

## Native endpoint

Through the native InsightIQ API, this operation is `GET /v1/professional/creators/dictionary/topics` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-professional-topics.md) for the provider-specific parameters and requirements.

