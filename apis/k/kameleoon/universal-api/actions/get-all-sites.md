# Kameleoon: Get all sites



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-sites?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-sites?${params}`, {
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
| `paramsIo` | string | yes | Required query object documented by Kameleoon for list endpoints. Example: `page=1, perPage=20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationFileUrl": "https://example.com",
      "code": "string",
      "currency": "string",
      "customSelectors": [
        "string"
      ],
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "domainNames": [
        "Ava Chen"
      ],
      "id": 1,
      "ignoreURLSettings": true,
      "kameleoonDomain": "string",
      "mainGoal": 1,
      "name": "Ava Chen",
      "siteType": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationFileUrl` | string |  |
| `code` | string |  |
| `currency` | string |  |
| `customSelectors` | array<string> |  |
| `dateCreated` | date |  |
| `description` | string |  |
| `domainNames` | array<string> |  |
| `id` | number |  |
| `ignoreURLSettings` | boolean |  |
| `kameleoonDomain` | string |  |
| `mainGoal` | number |  |
| `name` | string |  |
| `siteType` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Kameleoon API, this operation is `GET sites` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-sites.md) for the provider-specific parameters and requirements.

