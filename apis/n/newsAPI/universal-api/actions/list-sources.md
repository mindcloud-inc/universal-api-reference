# News API: List Sources

Retrieves top-headline news sources from News API.

```
GET https://connect.mindcloud.co/v1/universal/newsAPI/latest/actions/list-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a News API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsAPI/latest/actions/list-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsAPI/latest/actions/list-sources?${params}`, {
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
| `category` | string | no | Category of sources to return. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `language` | string | no | Language of sources to return. One of: `0`, `1`, `10`, `11`, `12`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `country` | string | no | Country of sources to return. One of: `0`, `1`, `10`, `11`, `12`, `13`, `14`, `15`, `16`, `17`, `18`, `19`, `2`, `20`, `21`, `22`, `23`, `24`, `25`, `26`, `27`, `28`, `29`, `3`, `30`, `31`, `32`, `33`, `34`, `35`, `36`, `37`, `38`, `39`, `4`, `40`, `41`, `42`, `43`, `44`, `45`, `46`, `47`, `48`, `49`, `5`, `50`, `51`, `52`, `53`, `6`, `7`, `8`, `9`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sources": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sources` | array<object> | The matching news sources returned by the request. |
| `status` | string | Response status from News API. |

## Native endpoint

Through the native News API API, this operation is `GET /top-headlines/sources` (base URL `https://newsapi.org/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sources.md) for the provider-specific parameters and requirements.

