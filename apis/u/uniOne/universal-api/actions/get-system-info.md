# UniOne: Get System Info

Retrieves account and usage details from UniOne.

```
GET https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-system-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-system-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-system-info?${params}`, {
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
      "accounting": {
        "emailsIncluded": 1,
        "emailsSent": 1,
        "periodEnd": "string",
        "periodStart": "string",
        "validationsIncluded": 1,
        "validationsUsed": 1
      },
      "email": "ava@example.com",
      "status": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounting.emailsIncluded` | number |  |
| `accounting.emailsSent` | number |  |
| `accounting.periodEnd` | string |  |
| `accounting.periodStart` | string |  |
| `accounting.validationsIncluded` | number |  |
| `accounting.validationsUsed` | number |  |
| `email` | string |  |
| `status` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native UniOne API, this operation is `POST system/info.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-system-info.md) for the provider-specific parameters and requirements.

