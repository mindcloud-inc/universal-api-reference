# Doppler Marketing Automation: Import Subscribers

Creates a subscriber import job in Doppler Marketing Automation.

```
POST https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/import-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Marketing Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/import-subscribers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fields[]": [
    "string"
  ],
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/import-subscribers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fields[]": ["string"],
    "items[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[]` | array<string> | yes | Required field-name list for import. Use an empty array when importing email-only subscribers. |
| `items[]` | array<object> | yes | Subscribers to import. |
| `callback` | string | no | Optional callback URL invoked when the import task completes. Example: `https://example.com/doppler/import-callback`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": [
        {}
      ],
      "createdResourceId": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | array<object> |  |
| `createdResourceId` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Doppler Marketing Automation API, this operation is `POST /accounts/:accountName/subscribers/import` (base URL `https://restapi.fromdoppler.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-subscribers.md) for the provider-specific parameters and requirements.

