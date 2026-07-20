# Edusign: Get School

Retrieves your school details from Edusign.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-school
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-school?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-school?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "absencesType": [
          {
            "id": 1,
            "name": "Ava Chen"
          }
        ],
        "city": "string",
        "connector": "string",
        "country": "string",
        "id": "string",
        "language": "string",
        "logo": "string",
        "logos": [
          {
            "filename": "Ava Chen",
            "url": "https://example.com"
          }
        ],
        "name": "Ava Chen",
        "nbCreditsDocumentLeft": 1,
        "phone": "string",
        "postalcode": "string",
        "signatureNb": 1,
        "streetAddress": "string",
        "timezone": "string",
        "webhooks": [
          {
            "type": "string",
            "url": "https://example.com"
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `result.absencesType` | array<object> |  |
| `result.absencesType[].id` | number |  |
| `result.absencesType[].name` | string |  |
| `result.city` | string |  |
| `result.connector` | string |  |
| `result.country` | string |  |
| `result.id` | string |  |
| `result.language` | string |  |
| `result.logo` | string |  |
| `result.logos` | array<object> |  |
| `result.logos[].filename` | string |  |
| `result.logos[].url` | string |  |
| `result.name` | string |  |
| `result.nbCreditsDocumentLeft` | number |  |
| `result.phone` | string |  |
| `result.postalcode` | string |  |
| `result.signatureNb` | number |  |
| `result.streetAddress` | string |  |
| `result.timezone` | string |  |
| `result.webhooks` | array<object> |  |
| `result.webhooks[].type` | string |  |
| `result.webhooks[].url` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v1/school` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-school.md) for the provider-specific parameters and requirements.

