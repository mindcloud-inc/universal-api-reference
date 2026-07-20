# HubSpot: Get Subscription by ID



```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-subscription-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-subscription-by-id?connectionId=$CONNECTION_ID&subscriptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-subscription-by-id?${params}`, {
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
| `subscriptionId` | string | yes | The unique ID of the subscription to retrieve. |
| `properties[]` | array<string> | no | Subscription properties to return in the response. |
| `propertiesWithHistory[]` | array<string> | no | Subscription properties to return with value history. |
| `associations` | string | no | Associated object types to include as associated IDs. |
| `archived` | boolean | no | Whether to return archived subscription records. |
| `idProperty` | string | no | The unique property to use for subscriptionId instead of the default record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the subscription is archived. |
| `createdAt` | date | The timestamp when the subscription was created. |
| `id` | string | The unique ID of the subscription. |
| `properties` | object | Key-value pairs representing the subscription properties. |
| `updatedAt` | date | The timestamp when the subscription was last updated. |
| `url` | string | The API URL for the subscription record when returned by HubSpot. |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/v3/objects/subscriptions/:subscriptionId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription-by-id.md) for the provider-specific parameters and requirements.

