# Simple Analytics: Add Website

Creates a new website in Simple Analytics.

```
POST https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/add-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simple Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/add-website" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hostname": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/add-website', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hostname": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hostname` | string | yes | Hostname to add, for example `example.com`. |
| `timezone` | string | no | IANA time zone for the new website. |
| `public` | boolean | no | Whether the website should be public. Default: `false`. |
| `label` | string | no | Optional label shown on the websites overview page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "ok": true,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Provider error message when website creation fails. |
| `ok` | boolean | Whether the website creation request was accepted. |
| `success` | boolean | Whether the website creation request succeeded. |

## Native endpoint

Through the native Simple Analytics API, this operation is `POST /api/websites/add` (base URL `https://simpleanalytics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-website.md) for the provider-specific parameters and requirements.

