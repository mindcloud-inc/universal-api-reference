# InsightIQ: Get Creator Topic Relevance

Retrieves creator topic relevance from InsightIQ.

```
GET https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-creator-topic-relevance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InsightIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-creator-topic-relevance?connectionId=$CONNECTION_ID&identifier=string&workPlatformId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string",
  "workPlatformId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-creator-topic-relevance?${params}`, {
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
| `identifier` | string | yes | Topic identifier obtained from the topics dictionary. |
| `workPlatformId` | string | yes | InsightIQ work platform identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
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
| `data` | array<object> |  |

## Native endpoint

Through the native InsightIQ API, this operation is `GET /v1/social/creators/dictionary/topics/relevance` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-creator-topic-relevance.md) for the provider-specific parameters and requirements.

