# Flexmail: Submit Opt-In

Creates an opt-in form submission in Flexmail.

```
POST https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/submit-opt-in
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexmail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/submit-opt-in" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "optInFormId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/submit-opt-in', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "optInFormId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes |  |
| `optInFormId` | number | yes |  |
| `firstName` | string | no |  |
| `name` | string | no |  |
| `language` | string | no |  |
| `customFields` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Placeholder schema for the documented no-content success response. |

## Native endpoint

Through the native Flexmail API, this operation is `POST /opt-ins` (base URL `https://api.flexmail.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-opt-in.md) for the provider-specific parameters and requirements.

