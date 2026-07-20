# Ninetailed: Update Locale



```
PUT https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/update-locale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninetailed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/update-locale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "environmentId": "master",
  "localeId": "string",
  "version": 1,
  "name": "Ava Chen",
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/update-locale', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "environmentId": "master",
    "localeId": "string",
    "version": 1,
    "name": "Ava Chen",
    "code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | Contentful space ID. |
| `environmentId` | string | yes | Contentful environment ID, such as master. Default: `master`. |
| `localeId` | string | yes | Locale resource ID to update. |
| `version` | number | yes | Current Contentful locale version for X-Contentful-Version. |
| `name` | string | yes | Locale display name. |
| `code` | string | yes | Locale code, such as en-US. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ninetailed API returns.

## Native endpoint

Through the native Ninetailed API, this operation is `PUT /spaces/:spaceId/environments/:environmentId/locales/:localeId` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-locale.md) for the provider-specific parameters and requirements.

