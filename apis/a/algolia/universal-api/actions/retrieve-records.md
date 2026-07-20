# Algolia: Retrieve Records

Retrieves records from one or more Algolia indices.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-records?connectionId=$CONNECTION_ID&requests%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requests[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-records?${params}`, {
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
| `requests[]` | array<object> | yes | Record lookup requests across one or more indices. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
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
| `results` | array<object> |  |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/indexes/*/objects` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-records.md) for the provider-specific parameters and requirements.

