# Atlar: Get holding activity

Retrieves a holding activity from Atlar.

```
GET https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-holding-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-holding-activity?connectionId=$CONNECTION_ID&pid=string&hid=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pid": "string",
  "hid": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/get-holding-activity?${params}`, {
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
| `pid` | string<string> | yes |  |
| `hid` | string<string> | yes |  |
| `id` | string<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": {},
      "created": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "etag": "string",
      "holdingId": "string",
      "id": "string",
      "metadata": {},
      "nav": {},
      "organizationId": "string",
      "portfolioId": "string",
      "scaledNav": {},
      "shares": 1,
      "tradeDate": "2026-05-07T12:00:00.000Z",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | object |  |
| `created` | date |  |
| `date` | date |  |
| `etag` | string |  |
| `holdingId` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `nav` | object |  |
| `organizationId` | string |  |
| `portfolioId` | string |  |
| `scaledNav` | object |  |
| `shares` | number |  |
| `tradeDate` | date |  |
| `type` | string |  |
| `updated` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Atlar API, this operation is `GET /financial-data/v2beta/portfolios/{pid}/holdings/{hid}/activities/{id}` (base URL `https://api.atlar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-holding-activity.md) for the provider-specific parameters and requirements.

