# Edusign: Update School

Updates your school details in Edusign.

```
PUT https://connect.mindcloud.co/v1/universal/edusign/latest/actions/update-school
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/update-school" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "school": {},
  "school.name": "Ava Chen",
  "school.logo": "string",
  "school.streetAddress": "string",
  "school.city": "string",
  "school.postalcode": "string",
  "school.country": "string",
  "school.phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edusign/latest/actions/update-school', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "school": {},
    "school.name": "Ava Chen",
    "school.logo": "string",
    "school.streetAddress": "string",
    "school.city": "string",
    "school.postalcode": "string",
    "school.country": "string",
    "school.phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `school` | object | yes |  |
| `school.name` | string | yes | School name |
| `school.logo` | string | yes | School logo |
| `school.streetAddress` | string | yes | School street address |
| `school.city` | string | yes | School city |
| `school.postalcode` | string | yes | School postal code |
| `school.country` | string | yes | School country |
| `school.phone` | string | yes | School phone |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `school.logos[]` | array<object> | no |  |
| `school.logos[]` | array<object> | no |  |
| `school.logos[]` | array<object> | no |  |
| `school.webhooks[]` | array<object> | no |  |
| `school.webhooks[]` | array<object> | no |  |
| `school.webhooks[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `PATCH /v1/school` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-school.md) for the provider-specific parameters and requirements.

