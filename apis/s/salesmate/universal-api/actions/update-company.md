# Salesmate: Update Company



```
PUT https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "name": "Ava Chen",
  "owner": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "name": "Ava Chen",
    "owner": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Salesmate company ID. |
| `name` | string | yes | Company name. |
| `owner` | number | yes | Salesmate user ID that owns the company. |
| `website` | string | no | Company website URL. |
| `phone` | string | no | Primary phone number. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `otherPhone` | string | no | Secondary phone number. |
| `currency` | string | no | Three-letter ISO currency code. |
| `description` | string | no | Internal company description. |
| `tags` | string | no | Comma-separated tag list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Salesmate API, this operation is `PUT /company/v4/:companyId` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

