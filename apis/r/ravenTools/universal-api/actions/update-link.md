# Raven Tools: Update Link

Updates an existing link in Raven Tools.

```
PUT https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/update-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raven Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/update-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "link": "JSON array with one Raven link record including link id and fields to update."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/update-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "link": "JSON array with one Raven link record including link id and fields to update."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `link` | string | yes | Default: `[{"tags":"single,updated","link id":"31311493","link text":"Single Raven Link Updated"}]`. Example: `JSON array with one Raven link record including link id and fields to update.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Raven Tools API returns.

## Native endpoint

Through the native Raven Tools API, this operation is `GET /api` (base URL `https://api.raventools.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-link.md) for the provider-specific parameters and requirements.

