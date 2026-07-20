# PageX: Add Lead



```
POST https://connect.mindcloud.co/v1/universal/pageX/latest/actions/add-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pageX/latest/actions/add-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pageX/latest/actions/add-lead', {
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
| `name` | string | no | Full name of the lead. |
| `email` | string | no | Email address of the lead. |
| `phone` | string | no | Phone number of the lead. |
| `plat` | string | no | Lead source platform, such as facebook, insta, or x. |
| `customerId` | string | no | Customer identifier when the source system already has one. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message describing the insert outcome. |
| `status` | string | Result state returned by the PageX lead endpoint. |

## Native endpoint

Through the native PageX API, this operation is `POST /api/lead` (base URL `https://www.pagexcrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-lead.md) for the provider-specific parameters and requirements.

