# EMnify: Get My Organization Details

Retrieves your organization details from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-my-organization-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-my-organization-details?connectionId=$CONNECTION_ID&authToken=Paste%20the%20auth_token%20from%20Retrieve%20Authentication%20Token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authToken": "Paste the auth_token from Retrieve Authentication Token"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-my-organization-details?${params}`, {
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
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. Example: `Paste the auth_token from Retrieve Authentication Token`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "class": {
        "description": "string",
        "id": 1
      },
      "country": {
        "countryCode": "string",
        "id": 1,
        "isoCode": "string",
        "mcc": "string",
        "name": "Ava Chen"
      },
      "created": "2026-05-07T12:00:00.000Z",
      "currency": {
        "code": "string",
        "id": 1,
        "symbol": "string"
      },
      "id": 1,
      "monthlyCostLimit": 1,
      "name": "Ava Chen",
      "relation": {
        "id": 1,
        "type": {
          "description": "string",
          "id": 1
        }
      },
      "status": {
        "description": "string",
        "id": 1
      },
      "type": {
        "description": "string",
        "id": 1
      },
      "verification": {},
      "verificationType": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `class.description` | string |  |
| `class.id` | number |  |
| `country.countryCode` | string |  |
| `country.id` | number |  |
| `country.isoCode` | string |  |
| `country.mcc` | string |  |
| `country.name` | string |  |
| `created` | date |  |
| `currency.code` | string |  |
| `currency.id` | number |  |
| `currency.symbol` | string |  |
| `id` | number |  |
| `monthlyCostLimit` | number |  |
| `name` | string |  |
| `relation.id` | number |  |
| `relation.type.description` | string |  |
| `relation.type.id` | number |  |
| `status.description` | string |  |
| `status.id` | number |  |
| `type.description` | string |  |
| `type.id` | number |  |
| `verification` | object |  |
| `verificationType` | object |  |

## Native endpoint

Through the native EMnify API, this operation is `GET /organisation/my` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-organization-details.md) for the provider-specific parameters and requirements.

