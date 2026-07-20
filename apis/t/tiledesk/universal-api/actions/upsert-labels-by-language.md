# Tiledesk: Upsert Labels By Language

Upserts labels for a language in Tiledesk.

```
PUT https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/upsert-labels-by-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiledesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/upsert-labels-by-language" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lang": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/upsert-labels-by-language', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lang": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lang` | string | yes | The label language code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "labels": {},
      "lang": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `labels` | object |  |
| `lang` | string |  |

## Native endpoint

Through the native Tiledesk API, this operation is `PUT /{{credentials.projectId}}/labels/:lang` (base URL `https://api.tiledesk.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-labels-by-language.md) for the provider-specific parameters and requirements.

