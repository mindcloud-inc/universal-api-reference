# ZeroBounce: Validate Email

Retrieves email validation details from ZeroBounce.

```
GET https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/validate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZeroBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/validate-email?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ipAddress` | string | no |  |
| `timeout` | number | no |  |
| `activityData` | boolean | no |  |
| `verifyPlus` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "address": "string",
      "city": "string",
      "country": "string",
      "didYouMean": "string",
      "domain": "string",
      "domainAgeDays": "string",
      "firstname": "Ava",
      "freeEmail": true,
      "gender": "string",
      "lastname": "Chen",
      "mxFound": "string",
      "mxRecord": "string",
      "processedAt": "string",
      "region": "string",
      "smtpProvider": "string",
      "status": "string",
      "subStatus": "string",
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `address` | string |  |
| `city` | string |  |
| `country` | string |  |
| `didYouMean` | string |  |
| `domain` | string |  |
| `domainAgeDays` | string |  |
| `firstname` | string |  |
| `freeEmail` | boolean |  |
| `gender` | string |  |
| `lastname` | string |  |
| `mxFound` | string |  |
| `mxRecord` | string |  |
| `processedAt` | string |  |
| `region` | string |  |
| `smtpProvider` | string |  |
| `status` | string |  |
| `subStatus` | string |  |
| `zipcode` | string |  |

## Native endpoint

Through the native ZeroBounce API, this operation is `GET /v2/validate` (base URL `https://api.zerobounce.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email.md) for the provider-specific parameters and requirements.

