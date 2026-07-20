# Boomlify: Create Email

Creates a new temporary email address in Boomlify.

```
POST https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/create-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boomlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/create-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/create-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customUsername` | string | no | Optional custom local-part for the generated temporary email address. |
| `time` | list | no | Optional email duration. Documented values are 10min, 1hour, 1day, and permanent. One of: `0`, `1`, `2`, `3`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | no | Optional custom domain for the generated email address. |
| `createAsDashboard` | boolean | no | Whether to create the address as a dashboard email. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Boomlify API returns.

## Native endpoint

Through the native Boomlify API, this operation is `POST /api/v1/emails/create` (base URL `https://v1.boomlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email.md) for the provider-specific parameters and requirements.

