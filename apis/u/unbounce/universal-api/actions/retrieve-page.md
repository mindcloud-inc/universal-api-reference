# Unbounce: Retrieve Page

Retrieves details for an Unbounce page.

```
GET https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/retrieve-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unbounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/retrieve-page?connectionId=$CONNECTION_ID&page_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/retrieve-page?${params}`, {
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
| `page_id` | string | yes | Unbounce page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "domain": "string",
      "id": "string",
      "integrations": [
        {}
      ],
      "integrationsCount": 1,
      "integrationsErrorsCount": 1,
      "lastPublishedAt": "string",
      "metadata": {},
      "name": "Ava Chen",
      "state": "string",
      "subAccountId": "string",
      "tests": {},
      "url": "https://example.com",
      "variantsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `domain` | string |  |
| `id` | string |  |
| `integrations` | array<object> |  |
| `integrationsCount` | number |  |
| `integrationsErrorsCount` | number |  |
| `lastPublishedAt` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `state` | string |  |
| `subAccountId` | string |  |
| `tests` | object |  |
| `url` | string |  |
| `variantsCount` | number |  |

## Native endpoint

Through the native Unbounce API, this operation is `GET /pages/:page_id` (base URL `https://api.unbounce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-page.md) for the provider-specific parameters and requirements.

