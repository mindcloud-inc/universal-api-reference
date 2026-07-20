# Tidio: Add Website as Lyro Data Source [Plus plan]

Adds a website as a Lyro data source in Tidio.

```
POST https://connect.mindcloud.co/v1/universal/tidio/latest/actions/add-website-as-lyro-data-source-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/add-website-as-lyro-data-source-plus-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidio/latest/actions/add-website-as-lyro-data-source-plus-plan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Website URL to scrape into a Lyro data source. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native Tidio API, this operation is `POST /lyro/data-sources/website/scrape` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-website-as-lyro-data-source-plus-plan.md) for the provider-specific parameters and requirements.

