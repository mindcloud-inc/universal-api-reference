# EyeLevel.ai: Crawl Website

Crawls a website into EyeLevel.ai for ingestion.

```
POST https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/crawl-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EyeLevel.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/crawl-website" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "websites": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/crawl-website', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "websites": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `websites` | list<object> | yes | An array of website crawl definitions to ingest. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ingest": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ingest` | object | Queued ingest process information. |

## Native endpoint

Through the native EyeLevel.ai API, this operation is `POST /ingest/documents/website` (base URL `https://api.groundx.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/crawl-website.md) for the provider-specific parameters and requirements.

