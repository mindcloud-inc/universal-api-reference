# ProvenExpert: Create Invitation Link

Creates a personal survey invitation link in ProvenExpert.

```
POST https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-invitation-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProvenExpert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-invitation-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.code": "VRTQ13",
  "data.email": "reviewer@example.org"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/provenExpert/latest/actions/create-invitation-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.code": "VRTQ13",
    "data.email": "reviewer@example.org"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.code` | string | yes | Survey code for which the personal invitation link should be created. Example: `VRTQ13`. |
| `data.email` | string | yes | Email address of the evaluator. Example: `reviewer@example.org`. |
| `data.name` | string | no | Name of the evaluator. Example: `John Doe`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exists": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exists` | number | Whether the evaluator email already has an invitation for the survey. |
| `url` | string | Personalized invitation link returned by ProvenExpert. |

## Native endpoint

Through the native ProvenExpert API, this operation is `POST /invite/url/create` (base URL `https://www.provenexpert.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invitation-link.md) for the provider-specific parameters and requirements.

