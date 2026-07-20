# Hireflix: List Position Shareable Links

Retrieves shareable links for a position in Hireflix.

```
GET https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-position-shareable-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-position-shareable-links?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-position-shareable-links?${params}`, {
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
| `variables.id` | string | yes | The Hireflix position ID. |
| `variables.shareableLinkId` | string | no | Optionally limit the response to a specific position shareable link ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowEvaluation": true,
      "companyId": "string",
      "createdAt": 1,
      "displayFunnelInformation": true,
      "dynamic": true,
      "expires": 1,
      "id": "string",
      "labels": [
        "string"
      ],
      "name": "Ava Chen",
      "owner": "string",
      "positionId": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowEvaluation` | boolean |  |
| `companyId` | string |  |
| `createdAt` | number |  |
| `displayFunnelInformation` | boolean |  |
| `dynamic` | boolean |  |
| `expires` | number |  |
| `id` | string |  |
| `labels` | array<string> |  |
| `name` | string |  |
| `owner` | string |  |
| `positionId` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-position-shareable-links.md) for the provider-specific parameters and requirements.

