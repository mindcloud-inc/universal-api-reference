# Pledge: Get Organization

Retrieves an organization from Pledge.

```
GET https://connect.mindcloud.co/v1/universal/pledge/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pledge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pledge/latest/actions/get-organization?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pledge/latest/actions/get-organization?${params}`, {
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
| `id` | string | yes | Organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "cause": "string",
      "causes": [
        {
          "id": 1,
          "name": "Ava Chen",
          "parentId": {}
        }
      ],
      "city": "string",
      "country": "string",
      "disbursementType": "string",
      "id": "string",
      "lat": "string",
      "logoUrl": "https://example.com",
      "lon": "string",
      "mission": "string",
      "name": "Ava Chen",
      "ngoId": "string",
      "postalCode": "string",
      "profileUrl": "https://example.com",
      "region": "string",
      "street1": "string",
      "street2": "string",
      "sustainableDevelopmentGoals": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `cause` | string |  |
| `causes[].id` | number |  |
| `causes[].name` | string |  |
| `causes[].parentId` | object |  |
| `city` | string |  |
| `country` | string |  |
| `disbursementType` | string |  |
| `id` | string |  |
| `lat` | string |  |
| `logoUrl` | string |  |
| `lon` | string |  |
| `mission` | string |  |
| `name` | string |  |
| `ngoId` | string |  |
| `postalCode` | string |  |
| `profileUrl` | string |  |
| `region` | string |  |
| `street1` | string |  |
| `street2` | string |  |
| `sustainableDevelopmentGoals[].id` | number |  |
| `sustainableDevelopmentGoals[].name` | string |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Pledge API, this operation is `GET /organizations/[:id]` (base URL `https://api.pledge.to/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

